---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/content/creating-custom-effects/generic-filter.html"
breadcrumb-title: ''
description: 學習如何為 Substance 3D Painter 製作通用濾鏡效果，以套用自訂的影像處理與貼圖濾鏡。
helpx_creative_field: ""
helpx_description: Painter > Content > Creating custom effects > Generic filter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 通用濾波器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---


# 通用濾波器

所有文件通道（包括不透明度）都會套用通用效果。 一般濾波器可以是：

* **灰階**&#x200B;會套用到每個通道的每個成分（底色、金屬色、粗糙度等）
* ****&#x200B;顏色則會直接套用在彩色通道上，或內部轉換成灰階以影響灰階通道

效果的輸入節點必須有&#x200B;**定義的識別**&#x200B;碼&#x200B;**或**&#x200B;使用&#x200B;**量定義**&#x200B;輸入，而其輸出節點必須有&#x200B;**輸出**。請注意， **基於顏色** 的調整器不能用於圖層的遮罩，只有 **灰階** 調整器能相容。

>[!NOTE]
>
> 在輸入節點中可以使用 **使用量** 或 **識別碼** （使用權優先權）。

範例：

![](../../assets/generic-filter.png)![](../../assets/generic-rgba.png){width="575px"}
