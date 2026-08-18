---
title: 位置
description: 學習如何使用 Substance 3D Painter 的位置產生器。
source-git-commit: b7770a9497f0db047433aec32c31b57f8dc13ae7
workflow-type: tm+mt
source-wordcount: '537'
ht-degree: 2%

---


# 位置

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../../assets/generators/icon_position.webp" alt=""/><br><strong>在：</strong> 網狀、紫外線、距離</td>
    <td style="border: 0;" valign="top"><strong>說明</strong><br>位置產生器利用烘焙的位置與世界空間法線貼圖，根據材質在三維空間中的位置（如上下或左右）建立漸層遮罩。<br><br>位置產生器輸出單色（黑白）紋理。 因此，它對於根據世界空間中的位置產生漸層遮罩非常有用。<br><br>需要烘焙的位置和世界空間法線貼圖作為影像輸入。 <a href="../../../baking/baking.md">在這裡了解更多烘焙知識</a>。</td>
  </tr>
</table>

## 輸入

| 輸入名稱 | 說明 |
| --- | --- |
| **材質** 色彩 | 使用自訂材質或錨點。 |
| **位置漸層** 顏色 | 使用烘焙的位置貼圖。 |
| **世界空間法線色彩** | 使用烘焙的世界空間法線貼圖。 |

## 參數

| 參數名稱 | 說明 |
| --- | --- |
| **全球反轉** | 所有效果合併後，將最終結果反轉。 |
| **全球模糊** | 在所有漸層合併後，均勻地模糊最終遮罩。 |
| **全球平衡** | 在所有漸層合成成黑白後，調整最終遮罩的平衡，就像亮度調整一樣。 |
| **全局對比** | 在所有漸層合併後，調整最終遮罩的對比度。 |
| **使用材質** | 切換自訂材質貼圖的使用開關。 |

### 位置梯度

| 參數名稱 | 說明 |
| --- | --- |
| **倒轉** | 只反轉位置梯度。 |
| **平衡** | 調整位置漸層的平衡，將中點像亮度控制一樣往黑或白移動。 |
| **對比** | 只調整位置漸層的對比度/衰減。 |
| **亮度** | 只調整位置梯度的亮度。 |
| **從右到左** | 調整效果在網格上的應用方式，從左到右。 |
| **從上到下** | 調整效果從上到下在網格上的套用方式。 |
| **從前到後** | 調整效果從前到後在網格上的套用方式。 |

#### 位置梯度/從右到左

| 參數名稱 | 說明 |
| --- | --- |
| **倒轉** | 將從右到左的漸變方向反轉。 |
| **混合模式** | 選擇從右到左漸層使用哪種 [混合模式](../../../interface/layer-stack/blending-modes.md) 。 |

#### 位置漸變/從上到下

| 參數名稱 | 說明 |
| --- | --- |
| **倒轉** | 將從上到下漸變的方向反轉。 |
| **混合模式** | 選擇 [從上到下漸層要使用的混合模式](../../../interface/layer-stack/blending-modes.md) 。 |

#### 位置漸變/前後

| 參數名稱 | 說明 |
| --- | --- |
| **倒轉** | 將前後漸變方向反轉。 |
| **混合模式** | 選擇 [前後漸層要使用的混合模式](../../../interface/layer-stack/blending-modes.md) 。 |

### 紋理

<table>
  <tr>
    <th>參數名稱</th>
    <th>說明</th>
  </tr>
  <tr>
    <td><strong>貼圖不透明度</strong></td>
    <td>調整自訂材質的可見度。</td>
  </tr>
  <tr>
    <td><strong>倒轉</strong></td>
    <td>反轉自訂材質貼圖。</td>
  </tr>
  <tr>
    <td><strong>灰階轉換</strong></td>
    <td>設定從全彩轉為灰階的方法。 <a href="grayscale-conversion.md">灰階轉換產生器提供更多關於每種方法運作</a>方式的資訊。</td>
  </tr>
  <tr>
    <td><strong>混合模式</strong></td>
    <td>選擇使用哪種 <a href="../../../interface/layer-stack/blending-modes.md">混合模式</a> 。</td>
  </tr>
  <tr>
    <td><strong>縮放</strong></td>
    <td>調整自訂材質的大小。</td>
  </tr>
  <tr>
    <td><strong>對比</strong></td>
    <td>調整自訂材質的對比度/衰減。</td>
  </tr>
  <tr>
    <td><strong>亮度</strong></td>
    <td>調整自訂材質的亮度。</td>
  </tr>
  <tr>
    <td><strong>三平面</strong></td>
    <td>啟用 <strong>Use Triplanear </strong>時，貼圖會從三個方向（X、Y、Z 軸）投影，而非僅依賴 UV。 <br><ul><li>沒有啟用三平面，貼圖會依照 UV 佈局。</li><li>啟用三平面時，貼圖會從多個角度投影並混合。</li></ul></td>
  </tr>
  <tr>
    <td><strong>三平面對比</strong></td>
    <td>用三平面貼圖調整投影時，材質融合的平滑程度。 這會調整來自不同方向投影之間的混合柔和度。</td>
  </tr>
</table>
