---
title: 夾子
description: 學習如何使用 Substance 3D Painter 的夾子濾鏡。
source-git-commit: 644a36a1dde953c1d793821e104049ebb6ec3c19
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 1%
---

# 夾子

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![夾具圖示](./Resources/icon_clamp.png "夾具")

<b>收錄於：</b> 效果/調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

夾持過濾器會將數值夾到定義的極限。

它可以直接用於填充層以限制材料的特定面向，或用於遮罩上以限制值在特定範圍內。

</td>
</tr>
</table>

>[!NOTE]
>
> 當用於填充層或作為色彩資訊的直通時，夾具會個別影響每個色彩通道。 因此，若某像素的顏色為 （R 0， G 0.5， B 1.0），且被夾為 0.5，該像素的顏色為 （R 0， G 0.5， B 0.5）。 這是因為藍色通道的數值足夠高可以被夾住，但其他通道沒有。 這表示夾具濾鏡可以改變有色內容的色調。
>
>如果你不想修改色調，像是 Levels 這類濾鏡可能會是更好的選擇。

<a name="parameters"></a>

## 參數

| 參數名稱 | 說明 |
| --- | --- |
| <b>Min：</b> | 調整最小值。 |
| <b>Max：</b> | 調整最大值。 |
