---
breadcrumb-title: ""
description: 學習如何在 Substance 3D Painter 中修正繪圖工具在 UV 島上的滲透問題，以維持乾淨的貼圖邊界。
title: Paint Tool 在其他 UV 島嶼上會滲色
user-guide-description: ""
user-guide-title: ""
source-git-commit: 6b6d52207ca1d043aaa1b2b14145b6b49d4c1942
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%
---

# Paint Tool 在其他 UV 島嶼上會滲色

在某些特定情況下，繪圖工具](../../../features/effects/paint.md)的預設行為[可能會顯得違反直覺。Substance 3D Painter 主要用於 3D 空間，這也適用於繪畫。 畫筆的預設設定是盡量在 UV 間無縫地畫畫。 這也是為什麼在與二維視角互動時，有些結果可能會讓人感到意外。

為了避免在 2D 視圖中繪製時其他 UV 島嶼出現出血問題，只要在工具參數中更改  **對齊**  設定：

| *對齊模式* | *預覽* |
| --- | --- |
| **切線包裹** | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../../assets/paint-mode-tangent-optim.gif"/></div> |
| **紫外線** | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../../assets/paint-mode-uv.gif" width="450px"/></div> |
