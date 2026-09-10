---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/content/importing-assets/adding-content-on-the-hard-drive.html"
breadcrumb-title: ''
description: 學習如何將硬碟內容加入 Substance 3D Painter，擴充本地檔案的資源庫。
helpx_creative_field: ""
helpx_description: Painter > Content > Importing assets > Adding content on the hard drive
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 在硬碟上新增內容
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---


# 在硬碟上新增內容

你可以透過將新內容直接放在硬碟的正確位置，為你的圖書館增添資源。

預設會有一個使用者素材資料夾，你可以透過應用程式介面或手動放置新內容，加入新的資料夾。 此預設函式庫也用於建立新預設，如筆刷、工具、智慧材質等。欲了解更多資訊，請參閱預設[&#128279;](../../painting/presets/presets.md)文件。

## 資產要放在哪裡？

以下是預設 **的 Your Assets** 庫位置，預設會在那裡建立你自己的自訂內容：

<table data-preserve-html="true" style="width: 100.0%;"><colgroup> <col style="width: 15.0%;"/> <col style="width: 15.0%;"/> <col style="width: 70.0%;"/> </colgroup><tbody><tr><th>平台</th><th>版本</th><th>路徑</th></tr><tr><td rowspan="2"><strong>窗戶</strong></td><td><strong>7.2</strong> 或更新版本</td><td colspan="1">C：\Users\username\Documents\Adobe\Adobe Substance 3D Painter</td></tr><tr><td colspan="1">遺產</td><td colspan="1">C：\Users\username\Documents\Allegorithmic\Substance Painter</td></tr><tr><td rowspan="2"><strong>麥克</strong></td><td colspan="1"><strong>7.2</strong> 或更新版本</td><td colspan="1">/使用者/使用者名稱/文件/Adobe/Adobe Substance 3D 畫家</td></tr><tr><td colspan="1">遺產</td><td colspan="1">/使用者/用戶名/文件/寓言/內容畫家</td></tr><tr><td rowspan="2"><strong>Linux</strong></td><td colspan="1"><strong>7.2</strong> 或更新版本</td><td colspan="1">/首頁/用戶名/文件/Adobe/Adobe Substance 3D 畫家</td></tr><tr><td>遺產</td><td colspan="1">/首頁/用戶名/文件/寓言/內容畫家</td></tr></tbody></table>

>[!WARNING]
>
> **隨應用程式附帶的 Starter 資產**&#x200B;位於安裝資料夾中，並在每個新版本中被替換。我們不建議將個人內容放在這裡，因為每次更新&#x200B;**都會被**&#x200B;刪除，甚至可能導致讀寫權限問題。\
> 最好使用 **「你的資產** 位置」或其他自訂位置。 欲了解更多如何新增自訂圖書館位置的資訊，請參見 [新增圖書館](../../interface/assets/adding-a-new-library.md)。

## 檔案格式與用途

你可以將不同類型的檔案匯入你的 Substance 3D Painter 函式庫。 將它們放入指定的資料夾（例如 *alpha、**colorluts*、*效果*......）會為資產分配使用方式，因此新增內容時選擇正確的資料夾非常重要。 請注意，如果你新增自訂的函式庫位置，系統會自動在該位置建立對應的資料夾。

| *檔案格式* | *使用情況* | *資料夾* |
| --- | --- | --- |
| **SBSAR** | 物質材料 | 資產 / 材料 |
| **SBSAR** | 濾鏡 | 資產 / 特效 |
| **SBSAR** | 發電機 | 資產 / 產生元 |
| **PNG、TGA、JPEG 等等。** | 材質或 Alpha | 資產 / 材質 **或** 書架 / Alpha |
| **HDR，EXR** | 環境或色彩lut | 資產 / 環境 **或** Shelf / Colorlut |
| **GLSL** | 著色器 | 資產 / 著色器 |
| **SPPR** | 刷子預設 | 資產 / 預設 / 筆刷 |
| **SPPR** | 粒子預設 | 資產 / 預設 / 粒子 |
| **SPPR** | 材質預設 | 資產 / 預設 / 材質 **或** 素材 / 素材 |
| **SPPR** | 工具預設 | 資產 / 預設 / 工具 |
| **SPSM** | 智慧材料 | 資產 / 智慧材料 |
| **SPMSK** | 智慧口罩 | 資產 / 智慧口罩 |
| **SPEXP** | 匯出預設 | 架式 / 匯出預設 |

>[!NOTE]
>
> 從 7.2.0 版本起，函式庫中可使用自訂資料夾與分類。 它們會在資產視窗中透過 [路徑](../../interface/assets/filter-by-path.md) 篩選或 [麵包屑](https://helpx.adobe.com/tw/substance-3d/unlisted/documentation/spdoc/navigating-in-the-shelf-147095659.html)存取。

>[!WARNING]
>
> **SBS** （非 SBSAR）檔案不能直接使用，必須從 Substance 3D Designer 匯出成 SBSAR。
