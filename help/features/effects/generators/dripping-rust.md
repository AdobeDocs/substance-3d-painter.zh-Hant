---
title: 滴落的鏽蝕
description: 學習如何使用Substance 3D Painter的滴落生鏽產生器。
source-git-commit: b7770a9497f0db047433aec32c31b57f8dc13ae7
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 1%

---


# 滴落的鏽蝕

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../../assets/generators/icon_dripping_rust.webp" alt=""/><br><strong>格式：</strong> 產生器、灰階、彩色</td>
    <td style="border: 0;" valign="top"><strong>說明</strong><br>滴落生鏽發生器會產生向下流動的鏽蝕條紋，模擬重力與水流造成的腐蝕。<br><br>滴落鏽蝕產生器輸出單色（黑白）材質。 因此，它在產生遮罩以產生滴落生鏽效果時非常有用。<br><br>影像輸入需要烘焙位置、曲率與環境遮蔽。 <a href="../../../baking/baking.md">在這裡了解更多烘焙知識</a>。</td>
  </tr>
</table>

## 輸入

| 輸入名稱 | 說明 |
| --- | --- |
| **曲率** 灰階 | 使用烘焙好的曲率地圖。 |
| **環境遮蔽** 灰階 | 使用烘焙好的環境遮蔽地圖。 |
| **位置** 顏色 | 使用烘焙的位置貼圖。 |

## 參數

<table>
  <tr>
    <th>參數名稱</th>
    <th>說明</th>
  </tr>
  <tr>
    <td><strong>種子</strong></td>
    <td>設定用來產生泥土材質的種子值。 <br><ul><li>點擊隨機可以切換到另一個隨機種子。</li><li>點擊鉛筆查看目前的種子值，若需要則輸入特定值。</li></ul></td>
  </tr>
  <tr>
    <td><strong>倒轉</strong></td>
    <td>在合成最終遮罩之前，先反轉特定的內部映射（例如曲率、AO）。</td>
  </tr>
  <tr>
    <td><strong>鏽蝕擴散</strong></td>
    <td>調整滴落生鏽效果的擴散。</td>
  </tr>
  <tr>
    <td><strong>鏽蝕對比</strong></td>
    <td>調整滴落生鏽效果的對比度。</td>
  </tr>
  <tr>
    <td><strong>擴散平滑度</strong></td>
    <td>調整滴落生鏽效果的膨脹柔軟度。</td>
  </tr>
  <tr>
    <td><strong>滴水強度</strong></td>
    <td>調整滴落生鏽效果的長度。</td>
  </tr>
  <tr>
    <td><strong>滴水的順滑度</strong></td>
    <td>調整滴落生鏽效果的柔和程度。</td>
  </tr>
  <tr>
    <td><strong>滴注樣本量</strong></td>
    <td>調整效果的品質（取樣數增加以提升音質）。</td>
  </tr>
  <tr>
    <td><strong>位置軸</strong></td>
    <td>在Y-Green通道、X-Red通道和B-Blue通道之間切換，可以改變滴落的鏽蝕效果方向。</td>
  </tr>
</table>
