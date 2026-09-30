---
title: 顏色配對
description: 學習如何在Substance 3D Painter中使用色彩匹配濾鏡。
source-git-commit: 644a36a1dde953c1d793821e104049ebb6ec3c19
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 1%
---

# 顏色配對

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="./Resources/icon_color_match.png" alt="顏色匹配圖示" title="顏色配對"/><br><strong>收錄於：</strong> 效果/調整</td>
    <td style="border: 0;" valign="top">描述<br>色彩匹配濾波器會將定義的來源色範圍與目標色範圍匹配，並支援輸入槽以定義來源與目標色值。 色彩匹配讓你在改變表面顏色的同時，保持細節，並控制色相、色度和亮度的處理方式。<br>色彩匹配用於填充層，進行細緻的色彩調整。</td>
  </tr>
</table>

## 輸入

| 輸入名稱 | 說明 |
| --- | --- |
| **來源顏色：** | 輸入槽用來輸入來源顏色。 使用自訂的色彩貼圖或錨點。 |
| **目標顏色：** | 目標顏色的輸入槽。 使用自訂的色彩貼圖或錨點。 |

## 參數

<table>
  <tr>
    <th>參數名稱</th>
    <th>說明</th>
  </tr>
  <tr>
    <td><strong>來源色彩模式：</strong></td>
    <td>選擇來源顏色的來源。<br><ul><li><strong>平均：使用</strong>現有材質顏色作為來源顏色。 注意，這需要將圖層混合模式設為 <strong>直通</strong>模式。</li><li><strong>參數</strong>：用參數設定來源顏色。</li><li><strong>輸入：用</strong>影像輸入設定來源顏色。</li></ul></td>
  </tr>
  <tr>
    <td><strong>來源顏色：</strong></td>
    <td>當 <strong>來源色彩模式</strong> 設為 <strong>參數</strong>時，請調整來源顏色。</td>
  </tr>
  <tr>
    <td><strong>目標色彩模式：</strong></td>
    <td>選擇目標顏色的來源。<br><ul><li><strong>參數：</strong>使用參數設定目標顏色。</li><li><strong>輸入：用</strong>影像輸入設定目標顏色。</li></ul></td>
  </tr>
  <tr>
    <td><strong>目標顏色：</strong></td>
    <td>當 <strong>目標色彩模式</strong> 設為 <strong>參數</strong>時，調整目標顏色。</td>
  </tr>
  <tr>
    <td><strong>自訂顏色變化：</strong></td>
    <td>切換自訂色調、色度和亮度變化控制。</td>
  </tr>
  <tr>
    <td><strong>Hue：</strong></td>
    <td>調整套用到結果的色調變化。</td>
  </tr>
  <tr>
    <td><strong>色度：</strong></td>
    <td>調整對結果施加的色度變化。</td>
  </tr>
  <tr>
    <td><strong>露瑪：</strong></td>
    <td>調整對結果施加的亮度變化。</td>
  </tr>
</table>