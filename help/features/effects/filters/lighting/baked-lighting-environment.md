---
title: 烘焙燈光環境
description: 學習如何使用 Substance 3D Painter 的烘焙光影環境濾鏡。
source-git-commit: 644a36a1dde953c1d793821e104049ebb6ec3c19
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 2%
---

# 烘焙燈光環境

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![烘焙光影環境圖示](./Resources/icon_baked_lighting_environment.png "烘焙光影環境")

<b>在：</b> 效果/光影、烘焙、環境、PBR

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 說明

烘焙光影環境過濾器將材質與環境光照資訊烘焙到色彩通道中。

它用於設定為直通模式的繪圖層，並套用到所有聲道。 它適用於不需要精確模擬光照，或資源有限的程式化工作流程，例如行動專案或僅依賴色彩貼圖的資產。

</td>
</tr>
</table>

## 輸入

| 輸入名稱 | 說明 |
| --- | --- |
| <b>環境遮蔽：</b> 灰階 | 使用烘焙好的環境遮蔽地圖。 |
| <b>環境地圖：</b> 灰階 | 使用環境地圖。 |
| <b>普通：</b> 顏色 | 使用烘焙好的法線貼圖。 |

<a name="parameters"></a>

## 參數

| 參數名稱 | 說明 |
| --- | --- |
| <b>水平旋轉：</b> | 調整環境燈光的水平旋轉。 |
| <b>垂直旋轉：</b> | 調整環境燈光的垂直旋轉。 |
| <b>暴露：</b> | 調整烘焙結果的曝光。 |
| <b>身高強度：</b> | 調整高度資訊對結果的影響程度。 |
| <b>環境遮蔽強度：</b> | 調整烘焙時環境遮蔽的強度。 |
| <b>鏡面遮蔽強度：</b> | 調整烘焙時鏡面遮蔽的強度。 |
