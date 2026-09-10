---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/getting-started/activation-and-licenses.html"
breadcrumb-title: ''
description: 學習如何啟用 Substance 3D Painter 並管理授權，開始使用該應用程式進行貼圖繪製。
helpx_creative_field: ""
helpx_description: Painter > Getting Started > Activation and licenses
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 啟動與執照
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 0%

---


# 啟動與執照

本頁有關於如何啟用和管理授權的資訊，讓你能開始使用 Painter。

## 依應用程式類型的啟動流程

啟動流程取決於你在哪裡購買或能使用Painter：

| 應用類型 | 啟動過程 |
| --- | --- |
| 創意雲端桌面 | 請參閱 HelpX 文件[&#128279;](https://helpx.adobe.com/tw/download-install/using/download-creative-cloud-apps.html)中的專屬頁面。若有任何問題， [Creative Cloud 的文件](https://helpx.adobe.com/tw/creative-cloud/user-guide.html) 可能會提供更多解答。 |
| 蒸汽 | 直接從你的 Steam 遊戲庫啟動產品。 |
| Substance 3D 獨立版 | 請參考下方說明的啟動流程。 |

## 獨立啟動步驟

### 啟動巫師

啟動巫師出現在某些舊版《Substance 3D Painter》中。

如果您在 2022 年 9 月 30 日前從 Substance 3D 網站下載了永久授權檔案，仍可透過啟用精靈啟用符合資格的 Substance 3D Painter 版本。 [關於舊有物質授權與帳號的更多資訊，請見此處。](https://substance3d.adobe.com/faq-end-of-life-accounts/)

![](../assets/activation-wizard.png){width="350px"}

啟動精靈有三個選項：

* <b>評估此產品</b>：舊有試驗已不再提供。 你可以在這裡 [或使用 Creative Cloud Desktop 開始為每個 Substance 3D 應用程式](https://www.adobe.com/tw/products/substance3d/free-trial-download.html?msockid=35568f9be2b964ec22d09c04e3eb65af) 開啟 30 天試用。
* <b>使用授權檔案</b>啟用：請於 2022 年 9 月 30 日前，使用從 Substance 3D 網站帳號頁面下載的授權檔案（<b>\*.key</b>）啟用產品。
* <b>使用您的帳戶</b>啟用：舊有物質帳戶已無法再用於啟用。

>[!WARNING]
>
> 要用啟用精靈安裝授權檔案，請確保你以管理員身份執行 Painter，並暫時停用防毒軟體。

### 手動啟動

你可以手動啟用 Substance Painter，方法是將 license.key 檔案放入以下資料夾：

>[!NOTE]
>
> 請確保檔案被呼叫 **license.key** 否則應用程式找不到。

<table data-preserve-html="true"><colgroup> <col/> <col/> <col/> <col/> </colgroup><tbody><tr><th>平台</th><th>版本</th><th colspan="2">路徑</th></tr><tr><td rowspan="4"><strong>窗戶</strong></td><td rowspan="2"><strong>7.2</strong> 或更新版本</td><td colspan="1">App Data（本地）</td><td colspan="1">C：\Users\[username]\AppData\Local\Adobe\Adobe Substance 3D Painter</td></tr><tr><td colspan="1">App Data（漫遊）</td><td colspan="1">C：\Users\[username]\AppData\Roaming\Adobe\Adobe Substance 3D Painter</td></tr><tr><td rowspan="2">遺產</td><td colspan="1">App Data（本地）</td><td colspan="1">C：\Users\[用戶名]\AppData\Local\Allegorithmic\Substance Painter</td></tr><tr><td colspan="1">App Data（漫遊）</td><td colspan="1">C：\Users\[用戶名]\AppData\Roaming\Allegorithmic\Substance Painter</td></tr><tr><td rowspan="2"><strong>麥克</strong></td><td colspan="1"><strong>7.2</strong> 或更新版本</td><td colspan="2">/使用者/[使用者名稱]/函式庫/應用程式支援/Adobe/Adobe Substance 3D 畫家</td></tr><tr><td colspan="1">遺產</td><td colspan="2">/使用者/[使用者名稱]/函式庫/應用程式支援/寓言/內容畫家</td></tr><tr><td rowspan="2"><strong>Linux</strong></td><td colspan="1"><strong>7.2</strong> 或更新版本</td><td colspan="2">/home/[username]/.local/share/Adobe/Adobe Substance 3D 畫家</td></tr><tr><td>遺產</td><td colspan="2">/home/[username]/.local/share/寓意/Substance Painter</td></tr></tbody></table>

>[!NOTE]
>
> 上述路徑中的部分目錄可能預設是隱藏的。 在檔案總管手動輸入路徑，或顯示隱藏檔案以查看。

### 環境變數

你可以用[環境變數覆蓋](../pipeline-and-integration/configuration/environment-variables.md) Painter 檢查 **license.key** 檔案的位置。
