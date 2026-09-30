---
title: PBR 驗證
description: 學習如何使用 Substance 3D Painter 的 PBR 驗證濾鏡。
source-git-commit: 644a36a1dde953c1d793821e104049ebb6ec3c19
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 2%
---

# PBR 驗證

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![PBR 驗證圖示](./Resources/icon_pbr_validate.png "PBR 驗證")

<b>在：</b> 效果/PBR、金屬、粗糙度

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

PBR 驗證濾波器透過檢查反照率暗值與金屬反射率範圍來驗證 PBR 資料。

它用於填充層，以驗證材料值是否維持在預期的PBR範圍內。 匯出材料時不應啟用 PBR 驗證。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

| 參數名稱 | 說明 |
| --- | --- |
| <b>驗證模式：</b> | 選擇要驗證反照率、金屬反射率，或兩者皆可。 |
| <b>反照率暗域閾值：</b> | 選擇允許的最小暗值閾值以進行反照率驗證。 |
| <b>金屬反射率範圍：</b> | 選擇用來驗證金屬值的反射率範圍。 |
| <b>疊加地圖：</b> | 切換驗證覆蓋在地圖資料上。 |

