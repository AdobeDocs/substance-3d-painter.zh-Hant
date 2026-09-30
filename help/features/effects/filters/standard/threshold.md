---
title: 臨界值
description: 學習如何使用Substance 3D Painter的Threshold濾鏡。
source-git-commit: 644a36a1dde953c1d793821e104049ebb6ec3c19
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 3%
---

# 臨界值

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![閾值圖示](./Resources/icon_threshold.png "門檻")

<b>收錄於：</b> 效果/調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

當輸入像素值相對於閾值值的比較標準符合模式參數設定時，閾值濾波器會回傳白色。 它類似直方圖掃描，但對比度始終維持在最大，提供更快且更精確的方式達成類似效果。

它可以直接用於填充層，或是用於遮罩（黑白輸出），以快速從特定通道建立高對比度遮罩。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

| 參數名稱 | 說明 |
| --- | --- |
| <b>門檻：</b> | 調整與輸入像素值比較的亮度值。 |
| <b>模式：</b> | 選擇以閾值為基準的比較標準：大、大或等、低或等。 |
| <b>_mode：</b> | 選擇內部模式值。 |
| <b>_threshold：</b> | 調整內部閾值。 |
| <b>_threshold_min：</b> | 調整內部最小閾值。 |
| <b>_threshold_max：</b> | 調整內部最大閾值。 |
