---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/workflow-issues/export-issues/texture-dilation-or-padding.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中使用貼圖膨脹和填充，以防止匯出貼圖出現邊緣失真。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Workflow Issues > Export Issues > Texture dilation or Padding
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 材質膨脹或填充
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 0%

---


# 材質膨脹或填充

**填充** （有時也稱為 **膨脹**）是紋理產生後發生的過程。 其目的是放大紫外線島的邊界，以填滿空白區域以相似像素。

產生高品質的填充很重要，這樣遊戲引擎或離線渲染器就能確保後續產生良好的 [mipmaps](../../../getting-started/glossary.md) 。\
Substance 3D Painter 可以產生無限填充：這表示像素會被拉伸直到到達另一個 UV 島嶼或貼圖邊界。

## 無限填充生成

以下是無限填充的運作範例：

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../assets/padding.gif){width="512px"}

</td>
<td style="border: 0;" valign="top">

![](../../../assets/padding-zoom.gif)

</td>
</tr>
</table>

## MipMaps

在3D電腦圖學中， **mipmap** 是預先計算、優化的紋理序列，每個紋理都是同一影像的逐步降低解析度表示。 它們旨在提升渲染速度並減少鋸齒雜訊。 高解析度的 mipmap 影像用於相機附近的物體。 當物體看起來較遠時，會使用較低解析度的影像。 這是一種有效率的渲染方式，而不是直接讀取原始材質中的所有像素。 每個層級的 mipmaps 會嵌入在材質本身（當檔案格式支援時）。

填充對 mipmap 非常重要，因為它能避免在使用較低材質解析度時，顏色滲透到 UV 內部。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../assets/mipmap-padding.gif){width="400px"}

</td>
<td style="border: 0;" valign="top">

![](../../../assets/mipmap-nopadding.gif){width="400px"}

</td>
</tr>
</table>

在上述範例中，灰色背景滲入 UV（右圖），而用填充後保持色彩乾淨（左圖）。

在 3D 應用中，結果如下：

![](../../../assets/padding-toggle.gif)

## 填充控制

Substance 3D Painter 允許在不同位置改變填充生成的行為（例如停用）：

* **烘焙時**：更多資訊請參閱[](../../../baking/baking.md)烘焙說明。
* **在為貼圖集** 產生貼圖時：更多資訊請參閱 [貼圖集設定](../../../interface/texture-set/texture-set-settings.md) 文件。
* **匯出貼圖**&#x200B;時：請參閱匯出設定](../../../export/export-window/export-window.md)文件中的[「填充設定」部分以獲得更多資訊。
