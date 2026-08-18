---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/baking/baking-visualization-settings.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中設定烘焙視覺化設定，以預覽和除錯網格貼圖烘焙結果。
helpx_creative_field: ""
helpx_description: Painter > Baking > Baking visualization settings
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 烘焙視覺化設定
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 1%

---


# 烘焙視覺化設定

![](../assets/viewport-vizu.png)

烘焙視覺化是在 Painter 的視窗內，當烘焙模式下顯示一個面板。 它允許你調整與 Viewport 中網格顯示相關的設定。

## 一般設定

| 背景設定 | 說明 |
| --- | --- |
| **隱藏烘焙網格** | 啟用後，這個圖示會隱藏視窗中的高多邊形和籠狀網格。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../assets/hide-baking-meshes.png"/></div> |
| **僅顯示選取的貼圖集** | 啟用後，目前啟用的材質集中只有籠狀和高多邊形網格會顯示在視窗中。 |

### 高解析度網狀網路（HP）

| 背景設定 | 說明 |
| --- | --- |
| <b>網狀</b> | 如果啟用，會在 3D 視圖中顯示高多邊形網格。 關閉後，高多邊形網格也會從記憶體中卸載，有助於提升效能。 請使用此設定旁的顏色選項來控制視窗中的網格表面顏色。 |
| <b>匹配誤差</b> | 如果啟用，則以指定顏色顯示籠子網格外殼外的高多邊形網格區域。 這種設定有助於辨識烘焙過程中容易被遺漏的區域，並可能導致細節或資訊遺失。 在此設定旁的色彩選項中，可以控制視窗中交叉區域的顏色。 |

### 籠子

| 背景設定 | 說明 |
| --- | --- |
| <b>籠子表面</b> | 啟用後，籠狀網格表面會顯示在 3D 視圖中。 籠子的表面是由設定旁邊的顏色按鈕定義的。 |
| <b>籠狀表面不透明度</b> | 讓網格變得多或少透明，以管理底層網格中細節的可見性。 |
| <b>籠式線框</b> | 啟用後，籠狀網格的線框會在視窗中顯示。 線框顏色可以用這個設定旁邊的顏色按鈕調整。 |
| <b>籠狀線框不透明度</b> | 讓線框圖更透明或更透明。 |

### 紫外線接縫

| 背景設定 | 說明 |
| --- | --- |
| <b>硬邊缺縫</b> | 啟用後，網格表面上非 UV 接縫的硬邊會以設定旁按鈕定義的顏色高亮顯示。 高亮邊緣只在籠子和低多邊形網格上可見。 邊緣在2D和3D視角中都能看到。 這個設定有助於辨識頂點法線分裂且沒有 UV 展開接縫的邊緣，這可能導致後續烘焙問題。 |

### 專案網格

<table data-preserve-html="true">
<colgroup><col/><col/><col/></colgroup><tbody><tr><th scope="col">背景設定</th>
<th scope="col">次要設定</th>
<th scope="col">說明</th>
</tr><tr><td><b>專案網格</b></td>
<td> </td>
<td><p>啟用後，烘焙高多邊形網格的低多邊形網格會在視口中顯示。 如果 <b>啟用了隱藏烘焙網格</b> ，這個設定也會自動啟用，以避免視窗空。</p>
<p>在此設定旁的顏色選項可調整專案網格的顏色。</p>
</td>
</tr><tr><td rowspan="7"><b>中性材料</b></td>
<td><b>品質</b></td>
<td>控制低多邊形網格表面的鏡面反射品質。 使用高數值會讓反射的真實度更好，但高數值會影響效能。 低值可能會在法線貼圖的陰影中產生接縫（注意：這只是顯示問題）。</td>
</tr><tr><td><b>粗糙度</b></td>
<td>控制視口中低多邊形網格材質的粗糙度。</td>
</tr><tr><td><b>金屬</b></td>
<td>控制視窗中低多邊形網格材質的金屬度。</td>
</tr><tr><td><b>AO 強度</b></td>
<td>控制烘焙的環境遮蔽對視口低多邊形網格著色的貢獻。</td>
</tr><tr><td><b>彎曲正常</b></td>
<td>如果啟用了，可以使用烘焙的彎曲法線來改善視口中低多邊形網格的陰影效果。</td>
</tr><tr><td><b>彎曲、正常、彌漫的量</b></td>
<td>控制彎曲法線對漫反射陰影的影響程度。</td>
</tr><tr><td><b>彎曲正常鏡面量</b></td>
<td>控制彎曲法線對鏡面陰影的影響程度。</td>
</tr></tbody></table>
