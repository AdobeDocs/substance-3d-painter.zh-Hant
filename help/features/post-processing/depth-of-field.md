---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/features/post-processing/depth-of-field.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中使用景深後製，創造逼真的相機對焦模糊效果。
helpx_creative_field: ""
helpx_description: Painter > Features > Post Processing > Depth of Field
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 景深
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---


# 景深

![](../../assets/dof-example.jpg)![](../../assets/dof.png)

**景深**（DOF）沒有直接參數。如果啟用，它會&#x200B;**覆蓋** Iray **的**&#x200B;景深。

為了控制視窗中景深的外觀，相機可設定兩種：

| *背景設定* | *描述* |
| --- | --- |
| **對焦距離** | 定義焦點所在的距離。  這個點被景深效果所利用。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/focus-distance-optim.gif"/></div> **注意：**  對焦距離可透過快捷鍵 **CTRL + 中鍵點擊網格的某一點自動設定。** |
| **光圈** | 定義景深的寬度。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/dof-aperture-optim.gif"/></div> **注意：**  如果 Iray 控制此參數，改變它會重新觸發計算。 |
