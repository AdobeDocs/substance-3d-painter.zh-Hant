---
title: 三維線性梯度
description: 學習如何使用 Substance 3D Painter 的 3D 線性漸層產生器。
source-git-commit: b095b9b437f75bbb3a3b85ee84a6850026c3bf98
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 1%

---


# 三維線性梯度

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../../assets/generators/icon_3d_linear_gradient.webp" alt=""/><br><strong>格式：</strong> 漸層、灰階</td>
    <td style="border: 0;" valign="top"><strong>說明</strong><br>3D 線性梯度產生器利用位置圖在網格上兩點之間建立梯度。 <br><br>3D 線性漸層輸出單色（黑白）紋理。 因此，它對於產生遮罩，在特定區域放置線性梯度非常有用。<br><br>需要一個烘焙位置圖作為影像輸入。 <a href="../../../baking/baking.md">在這裡了解更多烘焙知識</a>。<br><br>位置貼圖會為網格上的每個點分配顏色，對應其在 X、Y 和 Z 軸上介於 0 到 1 之間的位置。 這表示網格上的每個點都有獨特的顏色。 你可以透過選擇起點和終點的位置地圖顏色來設定線性漸層的起點和終點。</td>
  </tr>
</table>

## 輸入

| 輸入名稱 | 說明 |
| --- | --- |
| **職位** | 使用烘焙的位置貼圖。 |

## 參數

| 參數名稱 | 說明 |
| --- | --- |
| **倒轉** | 將線性梯度反轉。 |
| **平衡** | 移動線性梯度的中點位置。 |
| **對比** | 調整線性漸層的對比度。 |
| **3D 位置起始** | 根據位置圖的顏色設定漸層的起始點。 為了方便定義起始點，請在視窗螢幕上顯示位置圖，並使用色彩選擇器選擇起始點。 |
| **3D 位置結束** | 根據位置圖的顏色設定漸層的終點。 為了方便定義終點，可以在視窗螢幕上顯示位置圖，並使用色彩選擇器選擇終點。 |
