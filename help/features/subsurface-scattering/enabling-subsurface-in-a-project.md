---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/features/subsurface-scattering/enabling-subsurface-in-a-project.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 專案中啟用次表面散射，以創造逼真的半透明材質效果。
helpx_creative_field: ""
helpx_description: Painter > Features > Subsurface Scattering > Enabling Subsurface in a Project
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 專案中啟用地下水面
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---


# 專案中啟用地下水面

要在 Substance 3D Painter 中正確啟動 Subsurface 散射，必須先設定幾個參數。\
本頁提供應啟用參數的指引。

## 1 - 材質集設定

在 [貼圖集](../../interface/texture-set/texture-set.md) 中，如果尚未存在，請新增  **一個散射**  通道：

![](../../assets/add-channel.png)

>[!NOTE]
>
> 散射通道就像&#x200B;**覆蓋**&#x200B;表面&#x200B;**表面的遮罩**：如果通道是黑色，則沒有次表面;如果是白色，次表面強度會達到最大。這個通道是灰階值，預設&#x200B;**為**&#x200B;黑色。可以在圖層堆疊中加入填充層來控制預設顏色，或用繪畫圖層手動控制強度。

## 2 - 全球地下設定

在顯示設定[&#128279;](../../interface/display-settings/display-settings.md)（後期效果設定下方）啟用主要的次表面散射設定：

![](../../assets/enable-subsurface.png)

>[!NOTE]
>
> 啟用或停用 Subsurface 效果會影響整個專案。 如果這個全域參數在效能上太重，使用會很有幫助。

## 3 - 著色器設定

![](../../assets/shader-parameters.png)

在 Shader 設定[&#128279;](../../interface/shader-settings/shader-settings.md)視窗中，預設著色器可以找到一個「**SSS 參數**」群組，裡面有兩個設定。\
調整比例和顏色以符合目標材質。 關於這些設定的更多細節，請參見： [次表面參數](subsurface-parameters.md)

## 額外：啟用陰影

Subsurface 散射效果效果不錯，但單獨用可能會看起來怪怪的。\
啟用陰影能幫助視窗的最終效果，並提升最終材質的真實感。

在環境設定視窗中[，啟用「**陰影**」](../../interface/display-settings/environment-settings.md)設定：

![](../../assets/shadow-2.png)
