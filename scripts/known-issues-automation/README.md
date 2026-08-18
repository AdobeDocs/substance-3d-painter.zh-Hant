---
source-git-commit: 0376fe6500551442b28831d5742ecbbc9363ab19
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 0%

---
# 已知問題產生器 — Substance 3D Painter

自動化產生已知問題的 Substance 3D Painter 降價文件，發佈於：
`https://helpx.adobe.com/tw/substance-3d-painter/release-notes/know-issues.html`

本期內容取自Jira史詩 `SBSFOUR-6267`。 腳本會擷取所有問題，過濾目標版本中已修正的問題，並輸出一個格式化的 markdown 檔案，準備提交。

&#x200B;---

## 快速入門

這些步驟假設你已經完成了以下一次性設定。

1. 連接 **GlobalProtect VPN**
2. 在你的`.env`檔案中設定`TARGET_VERSION`為你要產生文件的版本（例如 `12.0.3`）
3. 從目錄執行腳本 `scripts/known-issues-automation/` ：

   ```
   python fetch_known_issues.py
   ```

4. 請查看輸出摘要——它會報告被檢取了多少期數、被排除了多少期
5. 將產生 `known-issues.md` 的 複製到 `help/release-notes/known-issues.md`

> 如果有任何缺失或意外的問題，請檢查 `raw_issues.json` Jira 在過濾前的回覆。

&#x200B;---

## 一次性設置

### &#x200B;1. 安裝相依

```bash
pip install requests python-dotenv
```

### &#x200B;2. 建立你的 `.env` 檔案

```bash
cp .env.example .env
```

### &#x200B;3. 取得 Jira 個人存取令牌

1. 登入 `https://jira.corp.adobe.com`
2. 請前往左側邊欄→ **個人存取令牌** 的個人資料
3. 點選 **建立代幣**，給它一個名稱，然後複製產生的值

> PATs 不會在瀏覽器會話結束時失效，因此比起腳本化 API 存取的會話 Cookie 更可靠。

### &#x200B;4. 填寫你的 `.env` 檔案

```
JIRA_PAT=your-personal-access-token
TARGET_VERSION=12.0.3
OUTPUT_FILE=known-issues.md
```

`TARGET_VERSION` 是你產生已知問題頁面的 Substance 3D Painter 版本。 它控制哪些固定問題被排除——詳見 [下方的過濾邏輯](#filtering-logic) 。

&#x200B;---

## 儲存庫結構

```
.
├── README.md                  # This file
├── fetch_known_issues.py      # Main script
├── .env.example               # Environment variable template (safe to commit)
├── .env                       # Your local credentials — never commit this
├── raw_issues.json            # Raw Jira dump from last run — gitignored
└── known-issues.md            # Generated output from last run — gitignored
```

&#x200B;---

## Jira 參考

| 場地 | 價值 |
|---|---|
| Jira 實例 | `https://jira.corp.adobe.com` |
| 專案關鍵 | `SBSFOUR` |
| 已知問題 史詩級 | `SBSFOUR-6267` |

所有已知議題必須與此史詩相關，才能出現在產生的文件中。 如果需要新增或移除某個問題，請在 Jira 中更新史詩，而不是手動編輯 markdown。

&#x200B;---

## 劇本運作原理

### 步驟一 — 取球

腳本會使用 JQL 查詢 Jira REST API：

```
"Epic Link" = SBSFOUR-6267 ORDER BY created ASC
```

結果頁碼為每頁50期。 每個議題會擷取以下欄位： `summary`， `issuetype`， `status`， `affectedVersions`， `fixVersions`， ， `labels`。

認證使用來自 `JIRA_PAT`的承載權杖。 企業 Jira 實例使用內部 SSL 憑證，因此這些請求會停用憑證驗證——這是 Adobe 網路上預期的行為。

### 步驟二 — 原始傾倒

在進行任何篩選或格式化之前，腳本會寫 `raw_issues.json`入 。 這是Jira回傳的每一期的簡化快照，無論接下來發生什麼，都會自動生成。 如果輸出看起來不對，請先檢查這個檔案——它精確顯示了 Jira 提供的資料。

### 步驟 3 — 過濾

議題會依兩條規則同時應用來篩選：

1. **狀態過濾器** — 只有 `Backlog` 和 `Dev In Progress` 問題是活躍的已知問題。 狀態問題 `Fixed` 可被排除，須依以下版本檢查。

2. **版本過濾器** — `Fixed` 只有當某個修正版本小於或 `TARGET_VERSION`等於 時，問題才會被排除。 如果修正版本高於 `TARGET_VERSION`，問題仍包含在內，因為修正尚未針對該版本發佈。

此方法處理兩個版本同時開發的情況：在 中`12.1.0`修正的問題仍然是已知的問題。`12.0.3`

完整決策表請參見 [過濾邏輯](#filtering-logic) 。

### 步驟 4 — 解析類別

每個議題摘要會在字串開頭解析類別標籤：

- `[Shader] Some description` →分類： `["Shader"]`、描述： `"Some description"`
- `[Crash][Engine] Some description` →分類： `["Crash", "Engine"]`、描述： `"Some description"`
- `No brackets here` →無分類，視為未分類

**主要類別**&#x200B;永遠是第一個標籤。它決定了分組和分段位置。

### 步驟五 — 分組與排序

各期的組織如下：

- 議題依主要類別分類
- 群組依序依序數量遞減（最大群組排前）
- 有多個問題的群組會出現在文件頂端
- 只有一期的群組，加上任何未分類的議題，會出現在多期群組之後，且沒有章節標題
- 以 為 `[Crash]` 主要類別的問題總是放在最後，在某 `## Stability` 個章節之下

### 步驟6 — 格式化並撰寫

腳本輸出 `known-issues.md` 為：

- YAML 前置件（helpx metadata）
- 標題 `# Known issues` 中有一個介紹段落，標示目標版本
- 問題格式如下： `` * `[Category]` Description ``
- 多類別議題： `` * `[Category1]` `[Category2]` Description ``
- 類別群組間的空白行
- 最後有 `## Stability` 一段關於當機問題的章節

&#x200B;---

## 過濾邏輯

| 現況 | 修正版本？ | 修正版本與目標版本 | 包含在內？ |
|---|---|---|---|
| `Backlog` | — | — | 是的 |
| `Dev In Progress` | — | — | 是的 |
| `Fixed` | 不 | — | 不（保守排除） |
| `Fixed` | 是的 | 修正目標≤版本 | 沒有（已經寄出） |
| `Fixed` | 是的 | 修正目標>版本 | 是的（修正會在未來版本中） |

&#x200B;---

## 輸出格式

```markdown
---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/release-notes/know-issues.html"
...
---

# Known issues

This page lists all the active known issues present in v12.0.3 of Substance 3D Painter:

* `[Engine]` Error when using Smart Materials if Texture Set has no tile 1001
* `[Engine]` Geometry mask shows artifacts at UV borders with instanced layers

* `[Shader]` user0 channel always can not be read as sRGB with specific shader

* `[Export]` GLTF exports at the wrong size
* `[Import]` Cannot import obj file with "nan" values

## Stability

* `[Crash]` Select "Export mesh" when mesh failed to load
```

**格式說明：** 類別標籤使用單一回溯勾標（single backtick）包裹—— `` `[Category]` `` 而非雙回標註。 舊有手動維護的文件包含雙回溯錯誤;腳本總是產生正確格式。

&#x200B;---

## 疑難排解

**401 未經授權**
- 確認你已連接 **GlobalProtect VPN**
- 你的PAT可能已經過期或被撤銷——請在新 `https://jira.corp.adobe.com/secure/ViewProfile.jspa` 時產生新的PAT並更新你的 `.env`

**`JIRA_PAT is not set`錯誤**
- 確保你已經建立`.env`&#x200B;`.env.example`並填寫了你的代幣檔案
- 確認你是在目錄裡`scripts/known-issues-automation/`執行腳本，這樣`python-dotenv`才能找到檔案`.env`

**輸出中缺少的問題**
- 檢查 `raw_issues.json` ——如果問題不存在，就代表它和 Jira 裡的 Epic `SBSFOUR-6267` 沒有關聯
- 如果問題在輸出 `raw_issues.json` 中但沒有，那就是過濾器排除了它——請檢查狀態並修正版本，對照你的 `TARGET_VERSION`

**`TARGET_VERSION`運行時警告**
- 劇本會執行，但如果`TARGET_VERSION`沒有設定，會保守地排除所有`Fixed`議題。一定要在產生最終文件前設定好。
