---
title: 三維距離
description: 學習如何使用 Substance 3D Painter 的 3D 距離產生器。
source-git-commit: b095b9b437f75bbb3a3b85ee84a6850026c3bf98
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 1%

---


# 三維距離

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../../assets/generators/icon_3d_distance.webp" alt=""/><br><strong>收錄於：</strong> mask、generator</td>
    <td style="border: 0;" valign="top"><strong>描述</strong><br>3D 距離產生器定義三維空間中的一個點（源點），並以單色漸層顯示該點的距離。 網格表面靠近點的區域顏色較暗，較遠的區域則較亮（預設）。<br><br>需要烘焙位置貼圖作為影像輸入。 <a href="../../../baking/baking.md">在這裡了解更多烘焙相關</a>資訊。<br><br>3D Distance 輸出的是單色（黑白）材質。 因此，它對於產生從特定位置遠方產生梯度的遮罩非常有用。<br><br></td>
  </tr>
</table>

## 輸入

| 輸入名稱 | 說明 |
| --- | --- |
| **職位** | 使用烘焙的位置圖來計算距離。 |

## 參數

| 參數名稱 | 說明 |
| --- | --- |
| **倒轉** | 反轉漸層。 |
| **位置X。** | 沿著 x 軸轉換來源點。 |
| **位置 Y** | 沿著 y 軸轉換源點。 |
| **位置Z** | 沿著 z 軸轉換來源點。 |
| **半徑** | 調整距離衰減的大小。 |
| **偏移** | 將梯度的起始和結束位置向或遠離源點移動。 遠離光源點（增加偏移量）會導致靠近光源點的暗區變大。 靠近來源點會讓漸層變淺，如果 **Offset** 設為 0，可能會完全移除。 |
| **對比** | 調整球形漸變的對比度。 |
