---
title: 填充區域遮罩
description: 學習如何使用 Substance 3D Painter 的填充區域遮罩濾鏡。
source-git-commit: 644a36a1dde953c1d793821e104049ebb6ec3c19
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 2%
---

# 填充區域遮罩

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![填充區域遮罩圖示](./Resources/icon_fill_area_mask.png "填充區域遮罩")

<b>在：</b> 效果/補色、形狀、輪廓、灰階

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

填充區域遮罩過濾器將輪廓轉換成填充形狀。 任何有連續邊界的區域都會被填滿。

它用於遮罩圖層（黑白輸出）圖層，並加入一層油漆以填補封閉的筆觸。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

| 參數名稱 | 說明 |
| --- | --- |
| <b>區域偵測：</b> | 選擇如何標示要填滿的區域。 |
| <b>區域偵測閾值：</b> | 調整區域偵測閾值。 |
| <b>除錯區域偵測：</b> | 透過區域偵測設定切換輪廓的顯示。 這有助於辨識尚未完全封閉的區域。 |
| <b>紫外線邊界行為：</b> | 選擇填滿區域時如何處理 UV 邊框。 |
| <b>紫外線邊界偵測閾值：</b> | 調整忽略原本可能被區域偵測填滿的紫外線區域的閾值。 |
