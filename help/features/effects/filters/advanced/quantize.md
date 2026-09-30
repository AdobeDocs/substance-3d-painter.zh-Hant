---
title: 量子化
description: 學習如何使用 Substance 3D Painter 的 Quantize 濾鏡。
source-git-commit: 644a36a1dde953c1d793821e104049ebb6ec3c19
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 1%
---

# 量子化

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![量化圖示](./Resources/icon_quantize.png "量化")

<b>收錄於：</b> 效果/量化、色彩

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

量化濾波器將影像簡化為有限的顏色集合。

它用於貼圖圖層，以創造較平坦、海報化或風格化的色彩區域。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

| 參數名稱 | 說明 |
| --- | --- |
| <b>顏色含量：</b> | 調整量化影像中使用的最大顏色數量。 此值也驅動擷取調色盤，儘管實際計數可能較低，取決於量化方法。 請查看調色盤色彩量輸出，以確認最終萃取的顏色數量。 |
| <b>輪廓平滑：</b> | 調整輸入影像所施加的平滑半徑，將量化結果簡化成更實體、更連貫的形狀。 較高的數值會明顯增加計算時間。 |
| <b>抖動：</b> | 調整用來重現漸層和色彩混合的抖動量，同時只使用量化後剩下的顏色。 使用輪廓平滑值為 0，以達到預期的抖動效果。 |
| <b>抖動模式：</b> | 選擇用於重現原始影像中漸層與色彩混合的抖動圖案。 |
| <b>距離色彩空間：</b> | 選擇量化時用於比較與分配色彩的色彩空間。 使用 Lab（Color）來處理感知色彩影像，RGB （Data）用於原始資料如法線貼圖。 |
| <b>申請 Alpha：</b> | 切換該層的 alpha 通道量化。 |
| <b>阿爾法門檻：</b> | 調整阿爾法門檻。 |

