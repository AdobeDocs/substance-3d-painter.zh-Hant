---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/technical-support/workflow-issues/shelf-issues/thumbnails-in-the-shelf-look-incorrect.html"
breadcrumb-title: ''
description: 學習如何修正 Substance 3D Painter 書架中錯誤的縮圖顯示，以確保資源預覽的準確度。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Workflow Issues > Shelf Issues > Thumbnails in the shelf look incorrect
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 架子上的縮圖看起來不對
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---


# 架子上的縮圖看起來不對

如果書架上的縮圖看起來和慣常不一樣，可能是因為用來渲染預覽的著色器不同。

| 壞掉的縮圖 | 一般縮圖 |
| --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../../assets/shelf-broken-preview.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../../assets/shelf-normal-preview.png" width="300px"/></div> |

## 1 - 開啟主設定視窗

請點  **選「編輯**  」並點選  **設定**  ：

![](../../../assets/pref-menu.png)

## 2 - 移除 Shelf 預覽著色器

在  **一般**  檢視中往下滑，直到「預覽選項」區塊可見。\
點擊&#x200B;**「**&#x200B;材質預覽著色器&#x200B;**」前方的十字**&#x200B;按鈕，即可移除目前指定的著色器。

![](../../../assets/remove-preview-shader.png){width="450px"}

## 3 - 重新啟動 Substance 3D Painter

為了重新生成縮圖使其看起來正確，Substance 3D Painter 需要重新啟動。
