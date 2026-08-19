---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/painting/fill-projections/fill-match-per-uv-tile.html"
breadcrumb-title: ''
description: 在 Substance 3D Painter 中使用 UV 圖塊的填充匹配，將紋理圖案在 UV 圖塊間匹配，實現無縫平鋪。
helpx_creative_field: ""
helpx_description: Painter > Painting > Fill projections > Fill (match per UV Tile)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 填充（以 UV 磚塊匹配）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 1%

---


# 填充（以 UV 磚塊匹配）

**填充（以 UV 圖塊匹配）**&#x200B;是一種特殊的 2D 投影，對 UV 圖塊[&#128279;](../../features/uv-tiles/uv-tiles.md)專案非常有用。它允許從序列中為每個 UV 圖塊指派 UDIM 貼圖。

這個投影沒有專門的設定，因為每個 UV 磚塊會被分配一張或多張圖片來填充。 由於沒有設定，這個模式在效能上也更好。

| 模式 | 說明 |
| --- | --- |
| **紫外線投影** | 所有 UV 圖塊會套用一張單一影像或序列中的第一個影像。 這同時也提供了變形控制，詳情請參見 [UV 投影](uv-projection.md) 。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/uv-3.jpg" width="700px"/></div> |
| **填充（以 UV 磚塊匹配）** | 序列中的每個影像都會分配到專用的 UV 圖塊。 沒有變形控制。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/fill-match.jpg" width="700px"/></div> |
