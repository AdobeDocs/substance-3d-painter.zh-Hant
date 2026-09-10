---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/painting/presets/photoshop-brush-presets-abr/photoshop-brush-parameters-compatibility.html"
breadcrumb-title: ''
description: 在 Substance 3D Painter 匯入 ABR 筆刷預設時，了解 Photoshop 筆刷參數的相容性。
helpx_creative_field: ""
helpx_description: Painter > Painting > Presets > Photoshop Brush Presets (ABR) > Photoshop Brush Parameters Compatibility
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Photoshop 筆刷參數相容性
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---


# Photoshop 筆刷參數相容性

本頁列出所有 Photoshop 筆刷參數及其與 Substance 3D Painter 筆刷引擎的相容性。

## 一般相容性

在 ABR 檔案中查看時，Substance 3D Painter 只會擷取特定的畫筆/工具預設：

| *預設類型* | *支持* | *描述* |
| --- | --- | --- |
| **刷子（點陣圖）** | 進口 | 根據點陣圖（bitmap）來刷刷預設，因為它們的 alpha 會被匯入。 |
| **刷子（程序劇）** | 被忽視 | 基於程序形狀（例如圓形）的筆刷預設不會被匯入。 |
| **刷子（噴筆）** | 被忽視 | 帶有噴筆設定的筆刷預設不會被匯入。 |
| **刷子（刷毛）** | 被忽視 | 帶有毛刺設定的筆刷預設不會被匯入。 |
| **刷子（可侵蝕）** | 被忽視 | 帶有可侵蝕設定的筆刷預設不會匯入。 |
| **鉛筆** | 被忽視 | 鉛筆預設不會被匯入。 |
| **混合刷** | 被忽視 | 混音器刷子預設不會匯入。 |
| **複製印章** | 被忽視 | Clone Stamp 預設不會被匯入。 |
| **污漬** | 被忽視 | Smudge 預設不會被匯入。 |

## 參數

想了解更多這些參數的功能，請參閱官方  [Photoshop 文件](https://helpx.adobe.com/photoshop/using/creating-modifying-brushes.html)  。

並非所有 Photoshop 筆刷參數都支援。 請參閱圖例以了解以下所述每個參數的狀態：

* **方格（■）**  表示該參數已支援，請參考描述以了解如何存取。
* **交叉（✖）**  表示該參數不被支援。

>[!NOTE]
>
> 雖然筆刷預設的控制參數可以透過筆傾斜、淡入淡出和筆壓等多種方式來控制，但目前僅  **支援筆壓**  。

| *團體* | *參數* | *支持* | *描述* |
| --- | --- | --- | --- |
| 筆尖形狀 | **規模** | ■ | 與繪圖工具尺寸參數相匹配。  **注意：**  Photoshop 以像素來定義尺寸，而 Substance 3D Painter 的尺寸則是基於專案 Bounding Box。 因此，完全吻合不可能，且僅為相對結果。 |
| **Flip X** | ■ | 透過「Brush Maker Photoshop」Substance 檔案處理。 |  |
| **翻轉 Y** | ■ | 透過「Brush Maker Photoshop」Substance 檔案處理。 |  |
| **角度** | ■ | 與繪圖工具的角度參數匹配。 |  |
| **圓度** | ■ | 透過「Brush Maker Photoshop」Substance 檔案處理。 |  |
| **硬度** | ■ | 透過「Brush Maker Photoshop」Substance 檔案處理。 |  |
| **間距** | ■ | 與 Paint 工具的間距參數相匹配。 |  |
|  |  |  |  |
| 形狀動力學 | **尺寸抖動** | ■ | 與繪圖工具尺寸抖動參數相匹配。 |
| **控制（用於大小）** | ■ | 搭配繪畫工具的壓力設定，尺寸參數。 |  |
| **最小直徑** | ■ | 與繪圖工具的最小尺寸參數相匹配。 |  |
| **傾斜刻度** | ✖ |  |  |
| **角度抖動** | ■ | 與繪圖工具的角度抖動參數匹配。 |  |
| **控制（代表角度）** | ✖ |  |  |
| **圓度抖動** | ■ | 透過「Brush Maker Photoshop」Substance 檔案處理。 |  |
| **最小圓度** | ■ | 透過「Brush Maker Photoshop」Substance 檔案處理。 |  |
| **翻轉 X 抖動** | ■ | 透過「Brush Maker Photoshop」Substance 檔案處理。 |  |
| **翻轉 Y 抖動** | ■ | 透過「Brush Maker Photoshop」Substance 檔案處理。 |  |
| **刷子投影** | ✖ |  |  |
|  |  |  |  |
| 散射 | **散射** | ■ | 與繪圖工具的位置抖動參數相匹配。 |
| **兩軸** | ■ | 與繪圖工具位置抖動軸參數匹配。 |  |
| **控制（針對散射）** | ✖ |  |  |
| **伯爵** | ■ | 透過繪圖工具的間距參數來補償。 |  |
| **吉特伯爵** | ✖ |  |  |
| **控制（代表 Count Jitter）** | ✖ |  |  |
|  |  |  |  |
| 紋理 | **紋理圖案** | ✖ |  |
| **倒轉** | ✖ |  |  |
| **規模** | ✖ |  |  |
| **亮度** | ✖ |  |  |
| **對比** | ✖ |  |  |
| **為每個尖端做紋理** | ✖ |  |  |
| **模式** | ✖ |  |  |
| **深度** | ✖ |  |  |
| **最低深度** | ✖ |  |  |
| **深度抖動** | ✖ |  |  |
| **控制（用於深度抖動）** | ✖ |  |  |
|  |  |  |  |
| 雙刷 | **模式** | ✖ |  |
| **規模** | ✖ |  |  |
| **間距** | ✖ |  |  |
| **散射** | ✖ |  |  |
| **兩軸** | ✖ |  |  |
| **伯爵** | ✖ |  |  |
|  |  |  |  |
| 色彩動態 | **按小費申請** | ✖ |  |
| **前景/背景抖動** | ✖ |  |  |
| **控制（用於 F/B 抖動）** | ✖ |  |  |
| **色相抖動** | ✖ |  |  |
| **飽和抖動** | ✖ |  |  |
| **亮度抖動** | ✖ |  |  |
| **純度** | ✖ |  |  |
|  |  |  |  |
| Transfert | **不透明度抖動** | ■ | 搭配 Paint 工具 Stamps 混合參數設定為「Lighten」。 |
| **控制（用於不透明度）** | ■ | 搭配 Paint 工具的壓力設定來設定流量參數。 |  |
| **最低（用於不透明度控制）** | ■ | 與繪畫工具的最小流量參數相匹配。 |  |
| **流動抖動** | ■ | 搭配繪圖工具的 Flow 抖動參數。 |  |
| **控制（用於流量）** | ■ | 搭配 Paint 工具的壓力設定，以設定流量參數（若低於不透明度）。 |  |
| **最小值（用於流量控制）** | ■ | 會搭配繪畫工具的最小流量參數（如果低於不透明度）。 |  |
| **濕度抖動** | ✖ |  |  |
| **控制（用於濕度抖動）** | ✖ |  |  |
| **最低限度（用於濕度控制）** | ✖ |  |  |
| **混合抖動** | ✖ |  |  |
| **控制（用於混音）** | ✖ |  |  |
| **最低限度（用於混音控制）** | ✖ |  |  |
|  |  |  |  |
| 刷式 | **傾斜X（Tilt X）** | ✖ |  |
| **覆寫傾斜X鍵** | ✖ |  |  |
| **傾斜Y型** | ✖ |  |  |
| **覆寫傾斜 Y** | ✖ |  |  |
| **旋轉** | ✖ |  |  |
| **覆寫旋轉** | ✖ |  |  |
| **壓力** | ✖ |  |  |
| **覆寫壓力** | ✖ |  |  |
|  |  |  |  |
| 其他 | **噪音** | ✖ |  |
| **濕邊** | ✖ |  |  |
| **積累過程** | ✖ |  |  |
| **平滑化** | ■ | 雖然不是直接匹配，但可以透過懶人鼠[&#128279;](../../lazy-mouse.md)設定來處理。 |  |
| **保護材質** | ✖ |  |  |
