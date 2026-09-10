---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/painting/text-resource.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中使用文字資源，將文字和排版加入你的貼圖繪畫工作流程。
helpx_creative_field: ""
helpx_description: Substance 3D Painter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 文本資源
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---


# 文本資源

![](../assets/v10_text_resource_banner-1.jpg)

<b>文本資源</b>可用於使用特定<b>字型檔案</b>將文字寫入紋理。有多種參數可用來調整最終文字的外觀。

## 瀏覽字型

要瀏覽可用的字型檔案，只需點擊資產視窗[&#128279;](../interface/assets/assets.md)中的字型過濾器（<b>T</b> 鍵）：

![](../assets/v10_text_assets.png)

字型也可以根據系統中位置依路徑進行篩選：

![](../assets/v10_font_path.png)

可用的字型位置依目前作業系統而異：

|  |  |
| --- | --- |
| 窗戶 | <ul data-preserve-html="true"> <li data-preserve-html="true"><b>系統</b>：C：/Windows/字型</li> <li data-preserve-html="true"><b>使用者</b>：c：/Users/username/Appdata/Local/Microsoft/Windows/字型</li> </ul> |
| MacOS | <ul data-preserve-html="true"> <li data-preserve-html="true"><b>系統</b>：/System/Library/字型</li> <li data-preserve-html="true"><b>本地：</b>/library/fonts</li> <li data-preserve-html="true"><b>使用者</b>：/使用者/使用者名/函式庫/字型</li> </ul> |
| Linux | <ul data-preserve-html="true"> <li data-preserve-html="true"><b>系統</b>：/usr/share/fonts/</li> <li data-preserve-html="true"><b>本地：</b>/usr/local/share/fonts/</li> <li data-preserve-html="true"><b>使用者</b>：/home/username/.local/share/fonts/</li> </ul> |

### 匯入字型

字型可以手動匯入，或像一般資源一樣放入現有的 Painter 函式庫。 要做到這點，請[&#128279;](../content/importing-assets/import-drag-and-drop.md)參考匯入文件。

Painter 支援.ttf<b></b>字型與 <b>.otf</b> 字型格式。

>[!NOTE]
>
> 如果資源無法載入/匯入並出現錯誤訊息「因字型授權限制無法匯入」，表示 Painter 無法使用該資源。 只能使用標示<b>為可</b>嵌入元資料的字型。

### 使用字型作為文字資源

貼圖資源的運作方式與其他資源（例如影像或 Substance 材質）類似，可用於畫筆參數、填充投影或 Substance 影像輸入。

要建立文字資源，只需在資源欄位中加入字型即可。 也可以在視窗中拖放字型。

![](../assets/v10_text_drag_drop.gif)

### 文字資源參數

文字資源具有以下基本參數：

![](../assets/v10_text_params_base.png)

| <b>參數</b> | <b>描述</b> |
| --- | --- |
| <b>正文</b> | 文字需要渲染。  **注意：**  介面中的文字欄位使用通用字型，字元範圍廣泛，可能導致輸入內容與所選字型在材質中能呈現的差異。 |
| <b>字體大小</b> | 指定計算字型大小的模式。 可用模式包括：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>自動</b>：大小是根據文字內容自動計算並貼合貼圖。</li> <li data-preserve-html="true"><b>自訂</b>：尺寸可以透過專用設定手動控制。</li> </ul> |
| <b>路線</b> | 控制垂直與水平的排列。 用按鈕選擇要使用的模式。 |
| <b>顏色</b> | 渲染文字的顏色。 若文字資源用於遮罩或灰階通道，此設定可能是灰階。 |

也有更進階的參數可供選擇：

![](../assets/v10_text_params_advanced.png)

| <b>參數</b> | <b>描述</b> |
| --- | --- |
| <b>行間距</b> | 相對於字型大小，文字行間距（「行首」）。 |
| <b>字元間距</b> | 相鄰字元間相對於字型大小的間距。 可以是負數來減去間距。 |
| <b>偏移</b> | 文字的水平與垂直偏移。 並正規化到字體大小。 |
| <b>背景填充</b> | 文字背後背景的顏色。 |
| <b>背景不透明度</b> | 背景色有多少是可見的？ |
| <b>解決方法</b> | 指定計算用於渲染文字的貼圖大小的模式。 可用模式包括：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>自動</b>：解析度會自動計算。</li> <li data-preserve-html="true"><b>自訂</b>：解析度可以透過專用設定手動定義。</li> </ul> |
