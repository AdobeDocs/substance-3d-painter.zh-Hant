---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/painting/advanced-channel-painting/flow-map-painting.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中繪製流圖，以控制材質流動方向與各向異性效果。
helpx_creative_field: ""
helpx_description: Painter > Painting > Advanced channel painting > Flow Map Painting
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 流程圖繪畫
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---


# 流程圖繪畫

計畫設置專用通道，但同時透過使用法線通道和一些筆刷參數，可以在 Substance 3D Painter 中繪製流程圖。

## 步驟 1：建立法線貼圖

建立一個 16 x 16 像素的法線貼圖貼圖。 顏色必須是 128、255、128，這應該會得到以下顏色： ![](../../assets/up-dx.png)\
（此顏色相當於 DirectX 中向上向量的現象）

## 步驟 2：新增一般通道

在你的 Substance 3D Painter 專案中，如果這個通道還沒有，請透過&#x200B;**貼圖集設定**&#x200B;新增一個&#x200B;**法線**&#x200B;通道。

## 步驟三：刷子設定

在筆刷參數中啟用跟隨路徑功能。 將法線貼圖貼圖（步驟1）載入法線通道槽。 關閉其他頻道。

![](../../assets/brush-settings-1.png){width="300px"}

## 步驟四：上色！

在網格上繪製並啟用跟隨路徑設定後，筆觸會將方向畫入法線貼圖。

![](../../assets/painting-1.png){width="700px"}
