---
source-git-commit: 6b6d52207ca1d043aaa1b2b14145b6b49d4c1942
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%
---
# 移除舊有的 HelpX 元資料

使用 Python 3.10 或更新版本，請從儲存庫根執行以下指令：

```shell
python remove_helpx_metadta.py 1 <path>
python remove_helpx_metadta.py 2 <path>
```

模式 `1` 是模擬考：列出匹配檔案並報告檔案數量掃描、有匹配的檔案，以及不更改檔案的元資料欄位。
模式 `2` 會移除這些欄位並報告移除次數。 省略 `<path>` 至掃描目前的資料夾。 引用路徑包含空格。

該腳本會遞迴掃描 `.md` 檔案（不區分大小寫），並移除頂層檔案名稱以 `helpx`開頭的 YAML 前件欄位，包括其多行價值觀。 它保留了其他元資料、註解、空白行、Markdown 內容，編碼與行尾。 它不會移除 `helpx` 正文中的參考。
使用模式 `2`前請先檢視試演;移除後會在不使用的情況下編輯檔案建立備份。 檔案錯誤及未封閉的前言內容會被報告並產生非零退出狀態。 未公開前段的檔案保持不變。