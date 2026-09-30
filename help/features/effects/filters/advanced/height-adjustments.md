---
title: 高度調整
description: 學習如何使用 Substance 3D Painter 的高度調整濾鏡。
source-git-commit: 644a36a1dde953c1d793821e104049ebb6ec3c19
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 1%
---

# 高度調整

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![高度調整圖示](./Resources/icon_height_adjust.png "高度調整")

<b>在：</b> 效果/調整、比例、偏移、反轉

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

高度調整濾波器會反演、偏移或乘以選定值。

它用於貼圖層或遮罩內部（黑白輸出），以非破壞性地調整高度資訊。

</td>
</tr>
</table>

<a name="parameters"></a>

## 參數

| 參數名稱 | 說明 |
| --- | --- |
| <b>反轉：</b> | 切換結果的反轉。 |
| <b>偏移：</b> | 透過加減指定長度來調整高度值。 |
| <b>乘法：</b> | 將高度值乘以此數值。 作為乘數，這會使較高區域較高，低區域降低。 |

>[!NOTE]
>
> **乘法**&#x200B;和&#x200B;**偏移**&#x200B;參數會疊加，偏移量會先套用。如果偏移在某點達到零，則乘法會乘以零，表示該點不會有任何變化。 要將乘法並偏移乘法，可以加第二個高度調整濾鏡。
