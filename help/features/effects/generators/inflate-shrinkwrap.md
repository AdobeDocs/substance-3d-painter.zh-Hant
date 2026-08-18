---
title: 充氣收縮膜
description: 學習如何使用Substance 3D Painter的充氣收縮包裝產生器。
source-git-commit: b7770a9497f0db047433aec32c31b57f8dc13ae7
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 3%

---


# 充氣收縮膜

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../../assets/generators/icon_inflate_shrinkwrap.webp" alt=""/><br><strong>格式：</strong> shrinkwrap、inflate、generator、randomseed</td>
    <td style="border: 0;" valign="top"><strong>說明</strong><br>：膨脹收縮膜產生器會增加皺褶，模擬薄層材料被拉伸覆蓋網格表面的效果。<br><br>膨脹收縮包裝產生器輸出單色（黑白）紋理。 因此，它對於產生產生收縮膜效果的遮罩非常有用。 不過，也可以直接放在填充圖層上，為高度和法線通道增加皺紋。<br><br>影像輸入需要烘焙的曲率貼圖。 <a href="../../../baking/baking.md">在這裡了解更多烘焙知識</a>。</td>
  </tr>
</table>

## 輸入

| 輸入名稱 | 說明 |
| --- | --- |
| **曲率** 灰階 | 使用烘焙好的曲率地圖。 |

## 參數

<table>
  <tr>
    <th>參數名稱</th>
    <th>說明</th>
  </tr>
  <tr>
    <td><strong>預設集</strong></td>
    <td>在充氣、真空拉動和緊繃預設之間切換。</td>
  </tr>
  <tr>
    <td><strong>種子</strong></td>
    <td>設定用來產生泥土材質的種子值。 <br><ul><li>點擊隨機可以切換到另一個隨機種子。</li><li>點擊鉛筆查看目前的種子值，若需要則輸入特定值。</li></ul></td>
  </tr>
  <tr>
    <td><strong>充氣或收縮包覆</strong></td>
    <td>在充氣和收縮膜模式之間切換。</td>
  </tr>
  <tr>
    <td><strong>縫隙強度</strong></td>
    <td>調整邊緣的突出程度。</td>
  </tr>
  <tr>
    <td><strong>凸起邊寬度</strong></td>
    <td>調整充氣邊緣收縮的程度。</td>
  </tr>
  <tr>
    <td><strong>邊緣強度提升</strong></td>
    <td>調整凸起邊緣效應的強度。</td>
  </tr>
  <tr>
    <td><strong>皺褶密度</strong></td>
    <td>調整皺紋的數量。</td>
  </tr>
  <tr>
    <td><strong>緊皺</strong></td>
    <td>調整皺紋在紫外線邊界的緊繃程度。</td>
  </tr>
  <tr>
    <td><strong>皺紋山脈</strong></td>
    <td>調整皺紋從紫外線邊界延伸的距離。</td>
  </tr>
  <tr>
    <td><strong>皺紋尺度</strong></td>
    <td>調整皺紋的大小。</td>
  </tr>
</table>

### 技術參數

| 參數名稱 | 說明 |
| --- | --- |
| **身高範圍** | 設定高度範圍。 |
| **身高位置** | 調整高度朝向黑色（0）或白色（1）。 |
| **表面積（公分）** | 設定表面的物理尺寸。 |
| **表面深度（公分）** | 設定表面的物理深度。 |
