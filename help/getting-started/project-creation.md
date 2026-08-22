---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/getting-started/project-creation.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中建立新專案，開始在你的 3D 模型上繪製貼圖。
helpx_creative_field: ""
helpx_description: Painter > Getting Started > Project Creation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 專案創建
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 0%

---


# 專案創建

![](../assets/v12_banner_project_window.jpg)

<b>新專案視窗</b>允許你建立專案檔案來儲存你的 3D 模型及其貼圖資訊。

根據匯入 3D 模型中找到的材質定義，建立新的 [材質集](../interface/texture-set/texture-set.md) 。 這表示只要物件材質不同，都可以透過同一個檔案匯入多個物件（即使 UV 重疊）。

## 創建新專案

要建立新專案，請點擊 <b>檔案>新建</b> ，或使用鍵盤快捷鍵 <b>Ctrl + N</b>。

以下是新專案視窗中所有參數的說明。

### 基本設定

| *參數* | *描述* |
| --- | --- |
| **檔案** | 點選「選擇」按鈕以指定要載入的 3D 模型檔案。 [支援的檔案格式清單可在此查閱。](https://experienceleague.adobe.com/zh-hant/docs/substance-3d/general-knowledge/ecosystem/import-and-export-formats) |
| **範本** | 指定一個範本，定義專案的預設設定。 範本包含以下參數：<ul data-preserve-html="true"> <li data-preserve-html="true">材質集設定。</li> <li data-preserve-html="true">顯示設定。</li> <li data-preserve-html="true">烘焙設定。</li> <li data-preserve-html="true">著色器資源（包括附加的貼圖）。</li> <li data-preserve-html="true">環境地圖檔案。</li> </ul>  **注意：**&#x200B;模板是 <b>\*.spt</b> 檔案，透過檔案選單[&#128279;](../interface/main-menu/file-menu.md)從現有專案建立，並儲存在 Assets 資料夾中，方便團隊成員分享。 |
| <b>解決方法</b> | 為每個材質集定義專案的預設材質解析度。 在應用程式內操作時，解析度最高可達 4K（4096x4096 像素），匯出時則可達 8K（8192x8192 像素）。 解析度可以在之後隨時透過 [材質集設定](../interface/texture-set/texture-set-settings.md)來更改。  **注意：**  8K 匯出至少需要 GPU 有 2.5GB VRam 才能使用。 |

### 檔案類型專屬設定

當選擇 USD 時，會開啟其他檔案類型的專屬設定。

| *參數* | *描述* |
| --- | --- |
| <b>範圍與變體</b> | 選擇 USD 檔案中的特定部分。 預設情況下，這個設定為「Root」，代表整個 USD 檔案都會用來建立 Painter 專案。  <b>找零......</b> 會打開一個新視窗，顯示美元內容。 若偵測到變體，可選擇特定變體來建立專案。 範圍與變體可在專案建立後，於 [專案設定](../interface/project-configuration.md) 中更改。 請注意——<ul data-preserve-html="true"> <li data-preserve-html="true">只有模型變體的選擇會對專案產生影響。</li> <li data-preserve-html="true">目前尚未偵測到嵌套於變異中的變異。</li> </ul> |
| <b>分區層級</b> | 對於應該細分的幾何體，這個設定允許你在 Painter 中指定想要細分多少網格以進行貼圖。 如果 USD 檔案中明確設定為「無」，這個設定會顯示灰色。  細分是在 UV 展開後套用，因此不會改變網格 UV 的形狀。 細分層級可在專案建立後，於 [專案設定](../interface/project-configuration.md) 中更改。 |
| <b>車架</b> | 對於偵測到動畫的 USD 檔案，這個設定允許你選擇用來建立 Painter 專案的幀。 如果選取的 USD 檔案中沒有動畫，這個設定會變成灰色。 框架可以在專案建立後，在 [專案設定](../interface/project-configuration.md) 中更改。 |

### 進階設定

| *參數* | *描述* |
| --- | --- |
| **法線貼圖格式** | 定義專案的法線貼圖格式，可以是以下一種形式。<ul data-preserve-html="true"><li data-preserve-html="true"><strong>DirectX</strong> （X+、Y-、Z+）</li><li data-preserve-html="true"><strong>OpenGL</strong> （X+、Y+、Z+）</li></ul>  **注意：**  提醒一下：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Unreal Engine</b> 預設使用 DirectX。</li> <li data-preserve-html="true"><b>Unity</b> 預設使用 OpenGL。</li> </ul> |
| **計算每個片段的切空間** | 啟用時，雙切線會在片段（像素）著色器中計算，而非頂點著色器。 這個參數會影響 Mark 貼圖在 viewport 中被 Shader 解碼的方式。 更改這些設定需要重新烘焙法線貼圖。  **注意：**  提醒一下：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Unreal Engine</b> 需要啟用這個設定。</li> <li data-preserve-html="true"><b>Unity</b> 需要將此設定關閉（或如果你使用 HDRP 工作流程則啟用）</li> </ul> |

### UV 圖塊設定（UDIM ）

>[!NOTE]
>
> 這些設定一旦建立專案就無法更改。

| *參數* | *描述* |
| --- | --- |
| **使用 UV Tile 工作流程** | 如果勾選，匯入的網格會被處理不同，允許在正常 UV 範圍（0-1）之外繪製。 使用 UDIM 的專案應該啟用此設定。 網格的處理方式可能因設定而異。 更多資訊請參閱 [UV Tile 文件](../features/uv-tiles/uv-tiles.md)。 |
| <b>保留每個材質的 UV 圖塊佈局，並啟用跨圖塊繪製</b> | UV 磚塊（UDIMs）會匯入並依照網格上的材質分配分組。 這表示單一材質集可以包含多個 UV 磚塊，並排在 2D 視圖中。 同一材質集內的 UV 圖塊可以無縫地塗裝。  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r2-column-c1_image_copy" src="../assets/uvtiles-paintacross.jpg" width="500px"/></div> |
| <b>將 UV 磚塊轉換成獨立的材質集（舊有）</b> | UV 圖塊（UDIMs）被拆分成獨立的貼圖集並重新命名，忽略任何材質分配。 每個 UV 圖塊會被移到 UV [0-1] 範圍以便可上色。  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r3-column-c1_image" src="../assets/uvtiles-legacy.jpg" width="500px"/></div> |

### 匯入設定

| ***參數*** | ***描述*** |
| --- | --- |
| **進口相機** | 如果網格檔案中有攝影機，它們會匯入專案並作為預設進行視覺化。  **注意：**  Substance 3D Painter 在某些條件下不支援某些攝影機：<ul data-preserve-html="true"><li data-preserve-html="true">3DS Max 的實體相機。</li><li data-preserve-html="true">正射相機儲存在 Alembic 檔案（&#42;.abc）中。</li></ul> |
| **自動展開** | 啟用後，匯入網格上會出現缺失的 UV。 處理方式可能會根據透過 **選項** 按鈕選擇的設定而有所不同。更多資訊請參閱 [自動 UV 展開文件](../features/automatic-uv-unwrapping.md)。 |

### 匯入烘焙地圖

使用<b>新增</b>按鈕將貼圖檔案載入為網格貼圖，並自動在貼圖集設定[&#128279;](../interface/texture-set/texture-set-settings.md)中指派。必須遵循特定的命名規則，才能自動將網格貼圖分配到其貼圖集。 網格貼圖也可以直接在應用程式內部烘焙;詳見烘焙文件。

命名慣例：<b> TextureSetName\_MeshMapName</b>

範例：<b> DefaultMaterial\_ambient\_occlusion.png </b>

支援的網格地圖列表及其命名：

| *網格貼圖* | *檔名慣例* |
| --- | --- |
| **環境遮蔽** | 環境音樂_occlusion |
| **曲率** | 曲率 |
| **正常** | 正常_base |
| **世界太空常態** | 世界\_space\_normals |
| **身分證** | 身分證 |
| **職位** | 職位 |
| **厚度** | 厚 |

### 實際大小

實體尺寸設定允許你調整 Painter 如何決定你在真實世界單位中網格的物理尺寸。 這有助於確保材料的貼面符合真實比例。

* 使用網格檔案的內部單位縮放：大多數檔案類型包含物件從 3D 建模應用程式匯出時的物理大小資訊。 選擇此選項後，Painter 將使用匯入檔案中的這些資訊。
* 自訂單位比例：覆寫匯入檔案的單位比例，若未包含單位比例，則使用自訂輸入框調整單一「單位」的大小。
* 指派材質時將填充層縮放切換為物理尺寸：啟用此功能後，擁有實體尺寸資訊的材質可以調整縮放，以符合所應用表面的物理尺寸。

### 色彩管理

![](../assets/newproj-cm.png)

此區塊控制專案的色彩管理設定。 預設設定為 Legacy（sRGB / 線性工作流程）。

可以看看 [色彩管理](../features/color-management/color-management.md) 文件，了解如何使用這個工作流程以及設定的功能。
