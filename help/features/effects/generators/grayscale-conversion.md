---
title: 灰階轉換
description: 學習如何使用 Substance 3D Painter 的灰階轉換產生器。
source-git-commit: b7770a9497f0db047433aec32c31b57f8dc13ae7
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 2%

---


# 灰階轉換

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../../assets/generators/icon_grayscale_conversion.png" alt=""/><br><strong>格式：</strong> 產生器、灰階、彩色</td>
    <td style="border: 0;" valign="top"><strong>說明</strong><br>：灰階轉換產生器會將材質或貼圖轉換成灰階值。<br><br>灰階轉換產生器輸出單色（黑白）材質。 因此，它對於從全色輸入映射產生遮罩非常有用。</td>
  </tr>
</table>

## 輸入

| 輸入名稱 | 說明 |
| --- | --- |
| **來源** 顏色 | 使用自訂的色彩貼圖或錨點。 |

## 參數

<table>
  <tr>
    <th>參數名稱</th>
    <th>說明</th>
  </tr>
  <tr>
    <td><strong>灰階類型</strong></td>
    <td>設定灰階轉換方法： <br><ul><li><strong>去飽和度</strong>：使用介於最強與最弱的 RGB 通道之間的數值。</li><li><strong>Luma</strong>：使用加權 RGB 係數，與人眼感知的亮度相符（偏向綠色）。</li><li><strong>平均</strong>：將紅、綠、藍三色通道均勻混合。</li><li><strong>Max</strong>：使用RGB頻道中最高的數值。</li><li><strong>最小</strong>值：使用RGB通道中最低的數值。<ul><li>紅色通道：只使用紅色通道。</li><li>綠色通道：僅使用綠色通道。</li><li>藍色頻道：僅使用藍色頻道。</li></ul></li></ul></td>
  </tr>
  <tr>
    <td><strong>倒轉</strong></td>
    <td>面具會反轉。</td>
  </tr>
  <tr>
    <td><strong>平衡</strong></td>
    <td>調整轉換後原始影像的平衡，將中點向黑或白移動，類似亮度控制。</td>
  </tr>
  <tr>
    <td><strong>對比</strong></td>
    <td>定義轉換後來源影像的對比度/衰減。</td>
  </tr>
  <tr>
    <td><strong>磚面</strong></td>
    <td>設定轉換後原始影像的平鋪。</td>
  </tr>
  <tr>
    <td><strong>旋轉</strong></td>
    <td>調整轉換後來源影像的角度。</td>
  </tr>
  <tr>
    <td><strong>安全旋轉</strong></td>
    <td>切換安全旋轉模式的開關。 當為真時，安全旋轉會鎖定旋轉至45度角。</td>
  </tr>
</table>
