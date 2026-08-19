---
title: 面具編輯器
description: 學習如何使用Substance 3D Painter的遮罩編輯器產生器。
source-git-commit: b7770a9497f0db047433aec32c31b57f8dc13ae7
workflow-type: tm+mt
source-wordcount: '1494'
ht-degree: 2%

---


# 面具編輯器

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../../assets/generators/icon_mask_editor_dark.png" alt=""/><strong>收錄於：</strong> mask、generator</td>
    <td style="border: 0;" valign="top"><strong>說明</strong><br>遮罩編輯器產生器是一款多功能遮罩產生器，讓你能將貼圖、Ambietn 遮蔽、曲率、世界空間法線、漸層、厚度和微觀細節合併成一個遮罩。<br>Mask Builder 產生器非常靈活，但由於其複雜性，對效能的影響比大多數產生器更大。<br><br>遮罩編輯器產生器輸出單色（黑白）材質。 因此，它對於根據各種烘焙的地圖產生遮罩非常有用。 <br><br>需要烘焙位置、厚度、曲率、環境遮蔽及世界空間法線貼圖作為影像輸入。 <a href="../../../baking/baking.md">在這裡了解更多烘焙知識</a>。</td>
  </tr>
</table>

## 輸入

| 輸入名稱 | 說明 |
| --- | --- |
| **材質** 色彩 | 使用自訂材質或錨點。 |
| **材質（次要）** 顏色 | 使用自訂材質或錨點。 |
| **世界空間法線色彩** | 使用烘焙的世界空間法線貼圖。 |
| **位置漸層** 顏色 | 使用烘焙的位置貼圖。 |
| **厚度** 灰階 | 使用烘焙的厚度貼圖。 |
| **曲率** 灰階 | 使用烘焙好的曲率地圖。 |
| **環境遮蔽** 灰階 | 使用烘焙好的環境遮蔽地圖。 |
| **微型標準** 色彩 | 使用自訂的法線貼圖或錨點。 |
| **微高** 色彩 | 使用自訂材質或錨點。 |

## 參數

| 參數名稱 | 說明 |
| --- | --- |
| **全球反轉** | 所有圖層合併後，將最終結果反轉。 |
| **全球模糊** | 在所有層疊合後均勻模糊最終遮罩。 |
| **全球平衡** | 在所有圖層合併成黑白後，調整最終遮罩的平衡，就像亮度調整一樣。 |
| **全局對比** | 在所有層合併後調整最終遮罩的對比度。 |
| **貼圖不透明度** | 調整自訂材質的可見度。 |
| **貼圖 2 不透明度** | 調整第二個自訂材質的可見性。 |
| **環境遮蔽不透明度** | 調整環境遮蔽細節的可見度。 |
| **曲率不透明度** | 調整曲率細節的可見度。 |
| **世界空間正常不透明度** | 調整世界空間的可見度，以及正常細節。 |
| **位置梯度不透明度** | 調整位置細節的可見度。 |
| **厚度不透明度** | 調整厚度細節的可見度。 |

### 紋理

<table>
  <tr>
    <th>參數名稱</th>
    <th>說明</th>
  </tr>
  <tr>
    <td><strong>倒轉</strong></td>
    <td>會反轉自訂材質。</td>
  </tr>
  <tr>
    <td><strong>灰階轉換</strong></td>
    <td>設定從全彩轉為灰階的方法。 <a href="grayscale-conversion.md">灰階轉換產生器提供更多關於每種方法運作</a>方式的資訊。</td>
  </tr>
  <tr>
    <td><strong>混合模式</strong></td>
    <td>選擇 <a href="../../../interface/layer-stack/blending-modes.md">目前圖層要使用的混合模式</a> 。</td>
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
  <tr>
    <td><strong>非方形鋪砌</strong></td>
    <td>切換非方形磁磚的開關。</td>
  </tr>
</table>

### 材質 2

<table>
  <tr>
    <th>參數名稱</th>
    <th>說明</th>
  </tr>
  <tr>
    <td><strong>倒轉</strong></td>
    <td>反轉自訂的次級貼圖。</td>
  </tr>
  <tr>
    <td><strong>灰階轉換</strong></td>
    <td>設定從全彩轉為灰階的方法。 <a href="grayscale-conversion.md">灰階轉換產生器提供更多關於每種方法運作</a>方式的資訊。</td>
  </tr>
  <tr>
    <td><strong>混合模式</strong></td>
    <td>選擇 <a href="../../../interface/layer-stack/blending-modes.md">目前圖層要使用的混合模式</a> 。</td>
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
  <tr>
    <td><strong>非方形鋪砌</strong></td>
    <td>切換非方形磁磚的開關。</td>
  </tr>
</table>

### 環境遮擋

| 參數名稱 | 說明 |
| --- | --- |
| **倒轉** | 反轉環境遮蔽和微細節圖層。 |
| **混合模式** | 選擇 [目前圖層要使用的混合模式](../../../interface/layer-stack/blending-modes.md) 。 |
| **模糊** | 調整環境遮蔽和微細節的柔和度。 |
| **平衡** | 調整環境光遮蔽和微觀細節的平衡，將中點像亮度控制一樣往黑或白移動。 |
| **對比** | 調整環境遮蔽和微細節的對比度/衰減。 |

### 曲率

<table>
  <tr>
    <th>參數名稱</th>
    <th>說明</th>
  </tr>
  <tr>
    <td><strong>倒轉</strong></td>
    <td>將曲率反轉。</td>
  </tr>
  <tr>
    <td><strong>混合模式</strong></td>
    <td>選擇 <a href="../../../interface/layer-stack/blending-modes.md">目前圖層要使用的混合模式</a> 。</td>
  </tr>
  <tr>
    <td><strong>模式</strong></td>
    <td>設定曲率模式。 <br><ul><li><strong>邊緣</strong>：遮罩邊緣（凸面區域）</li><li><strong>蛀牙</strong>：掩蓋蛀洞（凹陷區域）</li><li><strong>雙重：</strong>遮罩凹凸區域。</li><li><strong>未處理</strong>：正常曲面罩。</li></ul></td>
  </tr>
  <tr>
    <td><strong>銳利</strong></td>
    <td>調整銳利曲面細節的可見度。</td>
  </tr>
  <tr>
    <td><strong>好吧</strong></td>
    <td>調整細微曲率細節的可見度。</td>
  </tr>
  <tr>
    <td><strong>柔和</strong></td>
    <td>調整柔曲線細節的可見度。</td>
  </tr>
  <tr>
    <td><strong>中</strong></td>
    <td>調整中等曲率細節的可見度。</td>
  </tr>
  <tr>
    <td><strong>大</strong></td>
    <td>調整大曲率細節的可見度。</td>
  </tr>
  <tr>
    <td><strong>很大</strong></td>
    <td>調整大曲率細節的可見度。</td>
  </tr>
  <tr>
    <td><strong>巨大</strong></td>
    <td>調整巨大曲率細節的可見度。</td>
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

### 世界太空常態

| 參數名稱 | 說明 |
| --- | --- |
| **倒轉** | 反轉世界空間法線。 |
| **混合模式** | 選擇 [目前圖層要使用的混合模式](../../../interface/layer-stack/blending-modes.md) 。 |
| **模糊** | 調整世界空間的正常軟度。 |
| **平衡** | 調整世界空間法線的平衡，將中點向黑或白移動，就像亮度控制一樣。 |
| **對比** | 調整世界空間法線的對比度/衰減。 |
| **亮度** | 調整世界空間法線的亮度。 |
| **從右到左** | 調整效果在網格上的應用方式，從左到右。 |
| **從上到下** | 調整效果從上到下在網格上的套用方式。 |
| **從前到後** | 調整效果從前到後在網格上的套用方式。 |

### 世界空間法線/從右到左

| 參數名稱 | 說明 |
| --- | --- |
| **倒轉** | 將右向左反轉。 |
| **混合模式** | 選擇 [目前圖層要使用的混合模式](../../../interface/layer-stack/blending-modes.md) 。 |

### 世界空間標準/從上到下

| 參數名稱 | 說明 |
| --- | --- |
| **倒轉** | 將從上到下方向反轉。 |
| **混合模式** | 選擇 [目前圖層要使用的混合模式](../../../interface/layer-stack/blending-modes.md) 。 |

### 世界空間標準/從前到尾

| 參數名稱 | 說明 |
| --- | --- |
| **倒轉** | 將前向反轉為後方。 |
| **混合模式** | 選擇 [目前圖層要使用的混合模式](../../../interface/layer-stack/blending-modes.md) 。 |

### 位置梯度

| 參數名稱 | 說明 |
| --- | --- |
| **倒轉** | 反轉位置梯度層。 |
| **平衡** | 調整位置漸層的平衡，將中點向黑或白移動，就像亮度控制一樣。 |
| **對比** | 調整位置漸層的對比度/衰減。 |
| **亮度** | 調整位置梯度層的亮度。 |
| **混合模式** | 選擇 [目前圖層要使用的混合模式](../../../interface/layer-stack/blending-modes.md) 。 |
| **從右到左** | 調整效果在網格上的應用方式，從左到右。 |
| **從上到下** | 調整效果從上到下在網格上的套用方式。 |
| **從前到後** | 調整效果從前到後在網格上的套用方式。 |

>[!TIP]
>
> 位置梯度由最多三種梯度組成，分別是從右到左、從上到下，以及從前到後。 每個子漸層都有自己的混合模式，可以用來創造不同效果或遮罩模型的不同區域。 這些梯度的混合模式只會互相作用，形成最終的位置梯度圖層，不會直接與位置梯度外的其他圖層互動。

### 位置梯度 - 從右到左

| 參數名稱 | 說明 |
| --- | --- |
| **倒轉** | 將從右到左的漸變方向反轉。 |
| **混合模式** | 選擇從右到左漸層使用哪種 [混合模式](../../../interface/layer-stack/blending-modes.md) 。 |

### 位置漸變 - 從上到下

| 參數名稱 | 說明 |
| --- | --- |
| **倒轉** | 將從上到下漸變的方向反轉。 |
| **混合模式** | 選擇 [從上到下漸層要使用的混合模式](../../../interface/layer-stack/blending-modes.md) 。 |

### 位置漸變 - 從前到後

| 參數名稱 | 說明 |
| --- | --- |
| **倒轉** | 將前後漸變方向反轉。 |
| **混合模式** | 選擇 [前後漸層要使用的混合模式](../../../interface/layer-stack/blending-modes.md) 。 |

### 厚度

| 參數名稱 | 說明 |
| --- | --- |
| **倒轉** | 把厚度倒轉。 |
| **模糊** | 調整厚度層細節的柔和度。 |
| **對比** | 調整厚度層的對比度/衰減。 |
| **亮度** | 調整厚度層的亮度。 |

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
    <td>調整微高度細節的強度。</td>
  </tr>
  <tr>
    <td><strong>AO半徑</strong></td>
    <td>微細調整環境遮蔽的半徑（範圍）。</td>
  </tr>
  <tr>
    <td><strong>AO 深度</strong></td>
    <td>在微觀細節中調整環境遮蔽的深度（強度）。</td>
  </tr>
</table>
