---
title: 曲率
description: 學習如何使用 Substance 3D Painter 的曲率產生器。
source-git-commit: b095b9b437f75bbb3a3b85ee84a6850026c3bf98
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 2%

---


# 曲率

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../../assets/generators/icon_curvature.webp" alt=""/><br><strong>在：</strong> 遮罩、產生器、灰階、混合</td>
    <td style="border: 0;" valign="top"><strong>說明</strong><br>曲率產生器會根據烘焙的曲率貼圖建立遮罩，並可選擇將貼圖或微細節融合到遮罩中。<br><br>曲率產生器輸出單色（黑白）紋理。 因此，它在產生遮罩時比直接套用到圖層更有用。<br><br>需要一個烘焙好的位置貼圖作為輸入。 <a href="../../../baking/baking.md">在這裡了解更多烘焙知識</a>。</td>
  </tr>
</table>

## 輸入

| 輸入名稱 | 說明 |
| --- | --- |
| **材質** 色彩 | 使用自訂材質或錨點。 |
| **微型標準** 色彩 | 使用自訂的法線貼圖或錨點。 |
| **微高** 色彩 | 使用自訂材質或錨點。 |
| **曲率** 灰階 | 使用烘焙好的曲率地圖。 |
| **世界空間法線色彩** | 使用烘焙的世界空間法線貼圖。 |
| **位置漸層** 顏色 | 使用烘焙的位置貼圖。 |

## 參數

| 參數名稱 | 說明 |
| --- | --- |
| **全球反轉** | 在所有效果合併後，會反轉最終結果。 |
| **全球模糊** | 在所有效果合併後，最終遮罩會均勻柔化。 |
| **全球平衡** | 在所有效果合併後，會調整最終遮罩的平衡，從黑或白之間切換，就像亮度調整一樣。 |
| **全局對比** | 在所有效果合併後調整最終遮罩的對比度。 |
| **使用材質** | 切換自訂材質貼圖的使用開關。 |
| **使用微觀細節** | 開啟或關閉自訂微觀細節地圖的使用。 |

### 曲率

<table>
  <tr>
    <th>參數名稱</th>
    <th>說明</th>
  </tr>
  <tr>
    <td><strong>倒轉</strong></td>
    <td>將生成的曲率映射反轉。</td>
  </tr>
  <tr>
    <td><strong>模式</strong></td>
    <td>設定曲率模式。 <br><ul><li><strong>邊緣</strong>：遮罩邊緣（凸面區域）</li><li><strong>蛀牙</strong>：掩蓋蛀洞（凹陷區域）</li><li><strong>雙重：</strong>遮罩凹凸區域。</li><li><strong>未處理</strong>：正常曲面罩。</li></ul></td>
  </tr>
  <tr>
    <td><strong>銳利</strong></td>
    <td>調整銳利曲率細節的強度。</td>
  </tr>
  <tr>
    <td><strong>好吧</strong></td>
    <td>調整細微曲率細節的強度。</td>
  </tr>
  <tr>
    <td><strong>柔和</strong></td>
    <td>調整柔曲面細節的強度。</td>
  </tr>
  <tr>
    <td><strong>中</strong></td>
    <td>調整中等曲率細節的強度。</td>
  </tr>
  <tr>
    <td><strong>大</strong></td>
    <td>調整大曲率細節的強度。</td>
  </tr>
  <tr>
    <td><strong>很大</strong></td>
    <td>調整大曲率細節的強度。</td>
  </tr>
  <tr>
    <td><strong>巨大</strong></td>
    <td>調整那些巨大曲率細節的強度。</td>
  </tr>
  <tr>
    <td><strong>對比</strong></td>
    <td>調整曲率的對比度/衰減。</td>
  </tr>
  <tr>
    <td><strong>亮度</strong></td>
    <td>調整曲率的亮度。</td>
  </tr>
</table>

### 紋理

<table>
  <tr>
    <th>參數名稱</th>
    <th>說明</th>
  </tr>
  <tr>
    <td><strong>貼圖不透明度</strong></td>
    <td>控制自訂材質的可見性。</td>
  </tr>
  <tr>
    <td><strong>倒轉</strong></td>
    <td>只反轉自訂貼圖。</td>
  </tr>
  <tr>
    <td><strong>灰階轉換</strong></td>
    <td>選擇從彩色輸入轉換成黑白的方法。 </td>
  </tr>
  <tr>
    <td><strong>混合模式</strong></td>
    <td>設定自訂材質的混合模式。</td>
  </tr>
  <tr>
    <td><strong>縮放</strong></td>
    <td>調整自訂材質的大小。</td>
  </tr>
  <tr>
    <td><strong>對比</strong></td>
    <td>設定自訂材質的對比度/衰減。</td>
  </tr>
  <tr>
    <td><strong>亮度</strong></td>
    <td>設定自訂材質的亮度。</td>
  </tr>
  <tr>
    <td><strong>三平面</strong></td>
    <td>啟用三平面時，貼圖會從三個方向（X、Y、Z軸）投影，而不只依賴 UV。 <br><ul><li>沒有啟用三平面，貼圖會依照 UV 佈局。</li><li>啟用三平面時，貼圖會從多個角度投影並混合。</li></ul></td>
  </tr>
  <tr>
    <td><strong>三平面對比</strong></td>
    <td>用三平面貼圖調整投影時，材質融合的平滑程度。 這會調整來自不同方向投影之間的混合柔和度。</td>
  </tr>
</table>

### 微觀細節

<table>
  <tr>
    <th>參數名稱</th>
    <th>說明</th>
  </tr>
  <tr>
    <td><strong>微高</strong></td>
    <td>切換自訂微高度地圖的使用。</td>
  </tr>
  <tr>
    <td><strong>微型正常</strong></td>
    <td>切換自訂微法線貼圖的使用。</td>
  </tr>
  <tr>
    <td><strong>曲率類型</strong></td>
    <td>設定曲率類型。 <br><ul><li><strong>標準：</strong>通常能產生相當銳利的效果，但細節可能較寬。</li><li><strong>Sobel</strong>：與標準相近，但因使用索貝爾濾波器評估法線貼圖，畫面稍微模糊。</li><li><strong>平滑：</strong>產生不同層次的模糊（類似 mipmaps）以累積資訊。 這通常能提供更平滑的曲線，但細節可能會被忽略。</li></ul></td>
  </tr>
  <tr>
    <td><strong>曲率強度</strong></td>
    <td>在標準</strong>曲率和<strong>索貝爾</strong>曲率模式下調整曲率強度<strong>。</td>
  </tr>
  <tr>
    <td><strong>高度細節 強度</strong></td>
    <td>調整微高細節的強度。</td>
  </tr>
</table>
