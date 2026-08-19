---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/features/physical-size.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中設定實體尺寸，以定義真實世界的尺寸，以實現精確的貼圖縮放。
helpx_creative_field: ""
helpx_description: Painter > Features > Physical size
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 實際大小
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 2%

---


# 實際大小

![](../assets/banner-physicalsize-2.png)

物理尺寸是物質材料內部的一種特性，定義了它們的真實尺寸。 它能精確匹配材料在三維表面上的大小與外觀。 Painter 以公分作為預設的內部單位。

要使用物理尺寸，請套用一個具有此特性的材質，值非 0,0,0，然後在 UV 變換>縮放下，啟用填充層（或效果）中的物理尺寸模式。

欲了解更多資訊，請參閱：

* <b>填充投影中的</b>[物理尺寸參數](../painting/fill-projections/fill-projections.md)
* <b>視窗設定中的</b>[網格參數](../interface/display-settings/viewport-settings.md)
* <b>在著色器設定中</b>[，根據物理尺寸的位移](../interface/shader-settings/shader-settings.md)

>[!NOTE]
>
> * 從 Painter 8.3 版本起，所有類型的投影都可使用實體尺寸。
> * 大多數網格檔案格式會指定建立網格時使用的單位，匯入時會自動轉換成公分。
> * 有些格式，如 .obj，沒有單位資訊，因此當專案使用 .obj 網格建立時，預設會以公分為單位，且不會進行任何轉換。
