---
title: 汙垢
description: 學習如何使用Substance 3D Painter的泥土產生器。
source-git-commit: b7770a9497f0db047433aec32c31b57f8dc13ae7
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 1%

---


# 汙垢

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../../assets/generators/icon_dirt.webp" alt=""/><br><strong>收錄於：</strong> mask、generator</td>
    <td style="border: 0;" valign="top"><strong>說明</strong><br>Dirt 產生器根據曲率、環境遮蔽，在縫隙、邊緣和平坦表面上添加逼真的污垢與污垢堆積。 你也可以選擇使用微高度和微法線貼圖來增加更多細節。<br><br>Dirt 產生器輸出的是單色（黑白）材質。 因此，它對於產生遮罩，為模型增添污垢或髒污細節非常有用。<br><br>需要烘焙位置、曲率、環境遮蔽及世界空間法線貼圖作為影像輸入。 <a href="../../../baking/baking.md">在這裡了解更多烘焙知識</a>。</td>
  </tr>
</table>

>[!NOTE]
>
> 泥土產生器是一個強大的工具，可以快速將泥土加入你的網格中。 為了達到最佳效果，我們建議使用額外的遮罩來控制土壤的塗抹方式，並始終考慮資產的環境與歷史。

## 輸入

| 輸入名稱 | 說明 |
| --- | --- |
| **曲率** 灰階 | 使用烘焙好的曲率地圖。 |
| **環境遮蔽** 灰階 | 使用烘焙好的環境遮蔽地圖。 |
| **世界空間標準** 色 | 使用烘焙的世界空間法線貼圖。 |
| **位置** 顏色 | 使用烘焙的位置貼圖。 |
| **自訂垃圾搖滾** 灰階 | 使用自訂材質或錨點。 |
| **微型標準** 色彩 | 使用自訂的法線貼圖或錨點。 |
| **微高** 色彩 | 使用自訂材質或錨點。 |

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
    <td>把髒污面罩倒轉。</td>
  </tr>
  <tr>
    <td><strong>泥土等級</strong></td>
    <td>調整泥土效應的強度。</td>
  </tr>
  <tr>
    <td><strong>泥土對比</strong></td>
    <td>調整泥土效果的對比度。</td>
  </tr>
  <tr>
    <td><strong>使用三平面</strong></td>
    <td>啟用三平面時，貼圖會從三個方向（X、Y、Z軸）投影，而不只依賴 UV。 <br><ul><li>沒有啟用三平面，貼圖會依照 UV 佈局。</li><li>啟用三平面時，貼圖會從多個角度投影並混合。</li></ul></td>
  </tr>
  <tr>
    <td><strong>三面融合對比</strong></td>
    <td>用三平面貼圖調整投影時，材質融合的平滑程度。 它會調整從各個方向投影之間混合的柔和程度。</td>
  </tr>
  <tr>
    <td><strong>垃圾搖滾量</strong></td>
    <td>調整垃圾搖滾細節的強度。</td>
  </tr>
  <tr>
    <td><strong>垃圾搖滾等級</strong></td>
    <td>調整垃圾搖滾細節的大小。</td>
  </tr>
  <tr>
    <td><strong>使用自訂垃圾搖滾</strong></td>
    <td>切換自訂垃圾搖滾地圖的使用。</td>
  </tr>
  <tr>
    <td><strong>邊緣遮罩</strong></td>
    <td>根據曲率貼圖調整邊緣的遮罩。</td>
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
    <td>在標準曲率和索貝爾曲率模式下調整曲率強度。</td>
  </tr>
  <tr>
    <td><strong>高度細節 強度</strong></td>
    <td>調整微高細節的數量。</td>
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
