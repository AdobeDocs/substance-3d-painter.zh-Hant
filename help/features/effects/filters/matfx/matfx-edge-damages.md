---
title: MatFX Edge 損壞
description: 學習如何使用 Substance 3D Painter 的 MatFX Edge Damages 濾鏡。
source-git-commit: 644a36a1dde953c1d793821e104049ebb6ec3c19
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 1%
---

# MatFX Edge 損壞

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![MatFX Edge 損壞圖示](./Resources/icon_matfx_edge_damages.png "MatFX Edge 損壞")

<b>收錄於：</b> 特效/模糊、灰階

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

MatFX Edge Damages 濾鏡會產生剝落和損壞的邊緣細節。 Edge Damage 的行為與 MatFX Detail Edge Wear 濾鏡不同，Edge Damage 不會改變受損區域的顏色。 這表示它更適合模擬塑膠或樹脂等材料的損傷，而邊緣磨損則更適合用於塗裝金屬等材料。

MatFX Edge Damages 用於貼圖層或材質堆疊，以添加磨損、刮傷及損壞的邊緣細節。

</td>
</tr>
</table>

>[!NOTE]
>
> 為了讓 MatFX Edge Damages 濾波器修改高度通道，通道中必須有現有的高度資料。 換句話說，如果濾波器層下方沒有任何層有高度資料，濾波器就不會對高度通道產生可觀察的影響。

<a name="parameters"></a>

## 參數

| 參數名稱 | 說明 |
| --- | --- |
| <b>模糊強度：</b> | 調整模糊效果的強度。 |
| <b>模糊膜：</b> | 切換模糊包膜。 啟用時，效果會取樣材質另一側的像素。 |
| <b>等級：</b> | 調整整體傷害等級。 |
| <b>對比：</b> | 調整結果的對比度或衰減。 |
| <b>抓痕強度：</b> | 調整刮痕的強度。 |
| <b>損壞粗糙度：</b> | 調整受損區域的粗糙度。 |
| <b>損害深度：</b> | 調整受損區域的深度。 |
