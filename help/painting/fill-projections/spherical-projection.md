---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/painting/fill-projections/spherical-projection.html"
breadcrumb-title: ''
description: 在 Substance 3D Painter 中使用球面投影，從球體投影貼圖，將貼圖包裹在物件周圍。
helpx_creative_field: ""
helpx_description: Painter > Painting > Fill projections > Spherical projection
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 球面投影
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 0%

---


# 球面投影

![](../../assets/spherical-proj.jpg)

填充球面投影允許在物體周圍投射影像與圖案。 它可以在圓形物件上投射，或將紋理扭曲成圓形圖案。

## 屬性

| 背景設定 | 說明 |
| --- | --- |
| **過濾** | 控制材質或材質的過濾方式。 這個設定會影響重複使用時的材質外觀。 在高縮放值下，使用不同於預設的過濾方式，可能會產生更漂亮的效果。 目前可用的設定：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>雙線性 |HQ</strong> （預設）：進階雙線性濾波，嘗試在鋪磚值較高時提升紋理品質。</li><li data-preserve-html="true"><strong>雙線性 |銳利</strong>：簡單的雙線性濾波，稍微平滑紋理，但盡量保留細節。</li><li data-preserve-html="true"><strong>最近</strong>：無濾波，若雙線性濾波結果模糊且破壞細節，則有用。 可能會在貼圖中引入鋸齒。</li></ul> |
| **UV 包裹** | 控制貼圖在投影中的重複。 可能的數值包括：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>沒有</strong>：質地不會重複。 材質外的部分是黑色或透明的。</li><li data-preserve-html="true"><strong>橫向重複</strong>：質地只會橫向重複。</li><li data-preserve-html="true"><strong>垂直重複</strong>：紋理只會垂直重複。</li><li data-preserve-html="true"><strong>重複</strong> （預設）：材質在兩個軸上重複。</li></ul> <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/spherical-repeat.jpg" width="500px"/></div> |
| **形狀裁切** | 定義投影材質是否應該在投影區域外可見。 可能的數值包括：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>裁切成形</strong>的投影：投影被限制在投影區域內。</li><li data-preserve-html="true"><strong>投影延伸至外部形狀</strong> （預設：投影範圍會延伸至投影區域之外。</li></ul> <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r3-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/spherical-shape-crop.jpg" width="500px"/></div> |

### UV 轉換

UV 變換設定控制投影內的貼圖。

| *背景設定* | *描述* |
| --- | --- |
| **規模** | 定義貼圖在投影內會重複多少次。 |
| **旋轉** | 控制貼圖貼圖的角度。 |
| **偏移** | 控制投影材質的起點。 預設值代表材質位於投影的中間。 |

### 3D 投影設定

3D 投影設定控制投影在 3D 空間中的轉換。

| 背景設定 | 說明 |
| --- | --- |
| **偏移** | 投影在三維空間中原點的位置。 這些單位是根據整個場景的邊界框設計的。 0 是這個方框的中心。 |
| **旋轉** | 以度度為單位的角度，使整個投影在每個軸上旋轉。 |
| **規模** | 每個軸上的投影大小。 |

## 情境工具列

從位於視窗頂端的情境工具列](../../interface/toolbars.md)可使用[多項設定與工具，這些工具提供對操作手與投影的控制：

| 聖像 | 名稱 | 說明 |
| --- | --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r1-column-c0_image" src="../../assets/icon-hide-manipulator.png" width="50px"/></div> | 展示/隱藏操控者 | 啟用後，操作器會在視窗中可見且可控制。 |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r2-column-c0_image" src="../../assets/icon-manipulator-settings.png" width="50px"/></div> | 操作手設定 | 此選單包含三個設定：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>操作手的大小</strong>：控制操作手在視窗中的大小。</li><li data-preserve-html="true"><strong>格點步</strong>：在用約束平移時定義步長。</li><li data-preserve-html="true"><strong>角度步進</strong>：定義在有約束條件下旋轉時步進的角度。</li></ul> |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r3-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/icon-translate.png" width="50px"/></div> | 平移操作器 | 允許在場景中沿著主軸（X、Y、Z）移動投影。 |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r4-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/icon-rotate.png" width="50px"/></div> | 旋轉操作手 | 允許在場景中沿著主軸（X、Y、Z）旋轉投影。 |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r5-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/icon-scale.png" width="50px"/></div> | 比例操控器 | 允許在場景中沿著主軸（X、Y、Z）進行投影縮放。 |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r6-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/icon-surface.png" width="50px"/></div> | 表面操作手 | 允許透過將投影吸附在 3D 模型表面來移動投影。  **注意：**  此操作器僅適用於平面投影與扭曲投影類型。 |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r7-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/icon-space.png" width="50px"/></div> | 操作手空間 | 定義轉換在哪個空間進行。 可能的數值包括：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>局部空間</strong>：軸與電流變換對齊。</li><li data-preserve-html="true"><strong>世界空間</strong>：軸線會與場景對齊。</li></ul> |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r8-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/icon-flip-x.png" width="50px"/></div> | X上的鏡子 | 將轉換在 X 軸上反轉。 |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r9-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/icon-flip-y.png" width="50px"/></div> | Y字鏡 | 將轉換反轉到Y軸。 |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r10-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/icon-flip-z.png" width="50px"/></div> | Z 上的鏡子 | 將轉換方向在 Z 軸上反轉。 |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r11-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/icon-reset.png" width="50px"/></div> | 重置轉換 | 將投影轉換恢復到預設狀態。 |

## 操作手

此投影操作器僅在 [3D視窗](../../interface/viewport/3d-view.md)中提供。

| 動作 | 捷徑 | 說明 |
| --- | --- | --- |
| **翻譯** | 滑鼠點擊 | 使用平移操作器，點擊軸線可移動投影：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>一個軸</strong>：投影只向一個方向移動。</li><li data-preserve-html="true"><strong>兩個軸</strong>：將投影移動與軸對齊的平面圖。</li><li data-preserve-html="true"><strong>三個軸</strong>：在相機空間中移動投影（平面面向它）。</li></ul>   <table> <tr style="border: 0;"> <td style="border: 0;" valign="top">  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r1-column-c2_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/3d-translate.gif" width="200px"/></div>  </td> <td style="border: 0;" valign="top">  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r1-column-c2_dynamic_grid_items_grid-cell1_position-par_image" src="../../assets/3d-translate-2axes.gif" width="200px"/></div>  </td> <td style="border: 0;" valign="top">  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r1-column-c2_dynamic_grid_items_grid-cell2_position-par_image" src="../../assets/3d-translate-3axes.gif" width="200px"/></div>  </td> </tr> </table> |
| **翻譯受限** | SHIFT+滑鼠點擊 | 使用平移操作器，沿選定軸線移動投影，但僅在特定間隔（步進式）。 音程大小由操作手設定決定。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r2-column-c2_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/3d-translate-step.gif" width="200px"/></div> |
| **旋轉** | 滑鼠點擊 | 使用旋轉操作器，點擊其中一個軸即可旋轉投影。 點擊軸之間的位置可以同時旋轉所有軸。   <table> <tr style="border: 0;"> <td style="border: 0;" valign="top">  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r3-column-c2_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/3d-rotate.gif" width="200px"/></div>  </td> <td style="border: 0;" valign="top">  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r3-column-c2_dynamic_grid_items_grid-cell1_position-par_image" src="../../assets/3d-rotate-3axes.gif" width="200px"/></div>  </td> </tr> </table> |
| **旋轉受限** | SHIFT+滑鼠點擊 | 使用旋轉操作器時，點擊一個軸來旋轉投影只會在特定間隔發生。 這個階梯是由操作手設定的角度所定義。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r4-column-c2_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/3d-rotate-step.gif" width="200px"/></div> |
| **規模** | 滑鼠點擊 | 使用比例操作器，點擊一個軸柄，即可將投影沿著指定軸調整大小。   <table> <tr style="border: 0;"> <td style="border: 0;" valign="top">  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r5-column-c2_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/scale-one-axis.gif" width="200px"/></div>  </td> <td style="border: 0;" valign="top">  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r5-column-c2_dynamic_grid_items_grid-cell1_position-par_image" src="../../assets/scale-two-axis.gif" width="200px"/></div>  </td> <td style="border: 0;" valign="top">  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r5-column-c2_dynamic_grid_items_grid-cell2_position-par_image" src="../../assets/scale-3-axes.gif" width="200px"/></div>  </td> </tr> </table> |
| **規模受限** | SHIFT+滑鼠點擊 | 使用比例操作器時，點擊一個軸柄並維持快捷鍵，會分階段調整投影大小。 步長與平移操作器相同。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r6-column-c2_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/scale-1-axis-constrained.gif" width="200px"/></div> |
| **表面** | 滑鼠點擊 | 用 Surface Manipulator，點擊並拖曳它在 3D 模型上，就能把它吸附到表面上。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r7-column-c2_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/surface.gif" width="200px"/></div> **注意：**  此操作器僅 **適用於平面** 投影與 **扭曲** 投影類型。 |
