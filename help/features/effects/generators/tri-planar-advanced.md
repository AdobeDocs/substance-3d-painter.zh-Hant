---
title: 三位面進階
description: 學習如何使用Substance 3D Painter的Tri-Planear Advanced產生器。
source-git-commit: b7770a9497f0db047433aec32c31b57f8dc13ae7
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 1%

---


# 三位面進階

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../../assets/generators/icon_tri_planar_advanced.png" alt=""/><br><strong>收錄於：</strong> mask、generator</td>
    <td style="border: 0;" valign="top"><strong>說明</strong><br>三平面進階生成器是三平面混合模式的獨立版本，具備完整投影的手動控制，包括控制每個獨立軸的旋轉與偏移值。 與原生填充投影相比，Tri-Planear Advanced 生成器使用世界空間法線來混合三個投影軸，而原生實作僅依賴低多邊形幾何。 這會帶來更多的控制與更準確的結果。<br><br>Tri-Planear Advanced 產生器輸出單色（黑白）材質。 因此，它對於產生自訂遮罩或錨點的三平面混合作為遮罩非常有用。<br><br>需要烘焙的位置和世界空間法線貼圖作為影像輸入。 <a href="../../../baking/baking.md">在這裡了解更多烘焙知識</a>。</td>
  </tr>
</table>

## 輸入

| 輸入名稱 | 說明 |
| --- | --- |
| **世界空間標準** 色 | 使用烘焙的世界空間法線貼圖。 |
| **位置** 顏色 | 使用烘焙的位置貼圖。 |
| **遮罩** 灰階 | 使用自訂材質或錨點。 |

## 參數

<table>
  <tr>
    <th>參數名稱</th>
    <th>說明</th>
  </tr>
  <tr>
    <td><strong>投射</strong></td>
    <td>選擇是投影所有軸，還是只投影單一軸。</td>
  </tr>
  <tr>
    <td><strong>混合模式</strong></td>
    <td>選擇混合模式以跨軸混合。<br><ul><li><strong>線性</strong>：在線性混合模式下，混合過渡線是直線。</li><li><strong>進階</strong>：在進階混合模式中，軸是根據三個軸的最大值與指定位置的法線角度來混合。</li></ul></td>
  </tr>
  <tr>
    <td><strong>混合對比</strong></td>
    <td>調整混合過渡線模糊的程度。</td>
  </tr>
  <tr>
    <td><strong>貼圖平鋪</strong></td>
    <td>調整遮罩材質的平鋪。</td>
  </tr>
</table>

### 軸 X

| 參數名稱 | 說明 |
| --- | --- |
| **旋轉X階段** | 旋轉 X 軸材質投影。 |
| **偏移量 X X** | 將 X 軸材質投影向左或向右移動。 |
| **偏移量 X Y** | 將 X 軸材質投影往上或往下移動。 |

### 軸心 Y

| 參數名稱 | 說明 |
| --- | --- |
| **旋轉X階段** | 旋轉 Y 軸材質投影。 |
| **偏移 Y X** | 將 Y 軸材質投影向左或向右移動。 |
| **偏移 Y Y** | 將 Y 軸材質投影往上或往下移動。 |

### 軸 Z

| 參數名稱 | 說明 |
| --- | --- |
| **旋轉X階段** | 旋轉 Z 軸材質投影。 |
| **偏移Z X** | 將 Z 軸材質投影向左或向右移動。 |
| **偏移Z Y** | 將 Z 軸材質投影往上或往下移動。 |
