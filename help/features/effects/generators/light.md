---
title: 亮
description: 學習如何使用 Substance 3D Painter 的光源產生器。
source-git-commit: b095b9b437f75bbb3a3b85ee84a6850026c3bf98
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 2%

---


# 亮

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../../assets/generators/icon_light.webp" alt=""/><br><strong>收錄於：</strong> mask、generator</td>
    <td style="border: 0;" valign="top"><strong>說明</strong><br>光源會根據世界空間法線與位置貼圖，假裝有方向光照在你的網格上。<br><br>光源可用於填充層或作為遮罩。 當用於填充層時，產生器會輸出色彩、金屬度、鏡面粗糙度、法線和高度通道，這些通道可以多種組合來創造不同的效果。 我們建議在觀景窗中循環瀏覽頻道視角，了解每個頻道如何受到光源產生器的影響。<br><br>需要烘焙的位置和世界空間法線貼圖作為影像輸入。 <a href="../../../baking/baking.md">在這裡了解更多烘焙知識</a>。</td>
  </tr>
</table>

## 輸入

| 輸入名稱 | 說明 |
| --- | --- |
| **世界空間標準** 色 | 使用烘焙的世界空間法線貼圖。 |
| **位置** 顏色 | 使用烘焙的位置貼圖。 |

## 參數

| 參數名稱 | 說明 |
| --- | --- |
| **倒轉** | 將輸出的色彩映射反轉。 |
| **水平角** | 設定假燈的水平角度。 |
| **垂直角** | 設定假燈的垂直角度。 |
| **高光光澤** | 調整高亮區域的衰減擴散。 |
| **精彩片段等級** | 調整高光的對比度。 |
| **光衰減** | 調整光線衰減。 |
