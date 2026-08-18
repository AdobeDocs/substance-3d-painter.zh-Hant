---
title: 自動縫紉機
description: 學習如何使用 Substance 3D Painter 的自動縫紉生成器。
source-git-commit: b095b9b437f75bbb3a3b85ee84a6850026c3bf98
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 1%

---


# 自動縫紉機

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../../assets/generators/icon_auto_stitcher.png" alt=""/><br><strong>縫紉：</strong> 針，針</td>
    <td style="border: 0;" valign="top"><strong>說明</strong><br>：自動縫合器生成器會自動在程序生成的路徑上產生縫合效果。 這些路徑可以根據 UV 接縫、曲率或自訂輸入映射產生。<br><br>自動縫合器產生器輸出單色（黑白）材質。 因此，它在產生遮罩以套用縫合效果時非常有用。<br><br>要使用曲率遮罩模式，需要烘焙的曲率貼圖。 <a href="../../../baking/baking.md">在這裡了解更多烘焙知識</a>。</td>
  </tr>
</table>

## 輸入

<table>
  <tr>
    <th>輸入名稱</th>
    <th>說明</th>
  </tr>
  <tr>
    <td><strong>曲率</strong> 灰階</td>
    <td>選擇如何產生縫合路徑：<br><ul><li><strong>UV 遮罩</strong> 會產生沿著 UV 接縫的路徑。</li><li><strong>曲率 </strong>會在硬邊附近產生路徑。</li><li><strong>自訂輸入</strong> 讓你能透過地圖控制路徑生成的位置。<br>使用 <strong>自訂輸入</strong>時，路徑會在高對比區域產生。</li></ul></td>
  </tr>
  <tr>
    <td><strong>自訂輸入</strong> 灰階</td>
    <td>使用自訂材質或錨點。</td>
  </tr>
</table>

## 參數

<table>
  <tr>
    <th>參數名稱</th>
    <th>說明</th>
  </tr>
  <tr>
    <td><strong>遮罩模式</strong></td>
    <td>選擇「面罩模式」。<br><ul><li>UV 遮罩：基於 UV 島嶼的遮罩。</li><li>曲率：基於曲率地圖的面具。</li><li>自訂輸入：基於自訂輸入材質的遮罩。</li></ul></td>
  </tr>
  <tr>
    <td><strong>路徑平滑性</strong></td>
    <td>軟化縫線的路徑。</td>
  </tr>
  <tr>
    <td><strong>路徑位置</strong></td>
    <td>偏移路徑位置。</td>
  </tr>
  <tr>
    <td><strong>針法尺寸</strong></td>
    <td>調整針目比例。</td>
  </tr>
  <tr>
    <td><strong>針距</strong></td>
    <td>調整針目寬度。</td>
  </tr>
  <tr>
    <td><strong>針距</strong></td>
    <td>調整針目長度。</td>
  </tr>
  <tr>
    <td><strong>針法圓度</strong></td>
    <td>調整針腳的圓度。</td>
  </tr>
  <tr>
    <td><strong>抖動</strong></td>
    <td>調整針法的抖動和流向。</td>
  </tr>
</table>

## 範例

<table>
  <tr>
    <td><img src="../../../assets/generators/examples/auto-stitcher/custom-input2.png" alt=""/></td>
    <td>這個範例展示了自訂輸入如何產生縫合路徑。 <br><ul><li>黑白底色顯示我們用作自動縫合器產生器自訂輸入的噪音紋理。</li><li>自動縫合器生成器會遮蔽紅色層，讓紅色縫合路徑清晰可見。</li><li>注意紅色縫合路徑適合自訂輸入噪音紋理中足夠大的黑白區域。 紅色縫線從不從白色轉成黑色，也不會從黑色到白色。</li></ul><br>下圖展示了用來建立此範例的簡單圖層配置。<br><br><img src="../../../assets/generators/examples/auto-stitcher/custom-input-layer-stack.png" alt=""/></td>
  </tr>
</table>
