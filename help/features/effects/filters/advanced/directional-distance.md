---
title: 方向距離
description: 學習如何在 Substance 3D Painter 中使用方向距離濾鏡。
source-git-commit: 644a36a1dde953c1d793821e104049ebb6ec3c19
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 1%
---

# 方向距離

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="./Resources/icon_directional_distance.png" alt="方向距離圖示" title="方向距離"/><br><strong>收錄於：</strong> 效果/色彩、距離、方向性、漏水、雨</td>
    <td style="border: 0;" valign="top">描述<br>方向距離濾波器會產生沿指定方向移動的距離梯度。<br>它用於貼圖層，產生方向性條紋、洩漏及其他基於距離的效果。 你也可以用方向距離濾波器作為高度通道的遮罩，為你的正常通道增加立體感。</td>
  </tr>
</table>

## 輸入

| 輸入名稱 | 說明 |
| --- | --- |
| **距離圖：** 灰階 | 使用自訂材質或錨點。 |

## 參數

| 參數名稱 | 說明 |
| --- | --- |
| **距離：** | 調整標準化影像空間中距離梯度所移動的距離，其中 1 是輸入影像較短邊的長度。 |
| **角度：** | 調整轉彎時距離梯度的方向，0 在水平方向指向右側，或沿 （1,0） 向量。 |
| **對比：** | 調整結果的對比度或衰減。 |
| **距離地圖乘數：** | 調整距離貼圖對最大距離的影響程度。 當距離圖輸入未連接時，此參數不會產生影響。 |

## 範例

在下面的範例中，我們使用方向距離濾波器讓 Cells 2 產生器看起來像三維的。

![](../../../../assets/filters/directional-distance/3d.png)

這是透過建立一個填充圖層，啟用高度通道並設定為 1 來達成的。

接著在填充圖層加入黑色遮罩，並在遮罩中加入灰階設定為 **Cells 2** 的填充。 這會產生以下遮罩。

>[!NOTE]
>
> 你可以按住 Alt 並點擊遮罩圖示，在 Viewport 中查看遮罩&#x200B;**，或者在選取填充圖層後，使用 Viewport** 的&#x200B;**通道下拉選單選擇**&#x200B;遮罩&#x200B;**。**

![](../../../../assets/filters/directional-distance/cells2.png)

接著，在遮罩中新增一個濾波器，並選擇方向距離濾波器。

調整濾鏡設定以達到想要的效果，但遮罩應該會像下面的範例一樣。

![](../../../../assets/filters/directional-distance/result.png)

切回材質檢視，可以看到視窗中的效果。
