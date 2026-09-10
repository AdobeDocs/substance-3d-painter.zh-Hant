---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/content/creating-custom-effects/mesh-based-input.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 的自訂效果中使用基於網格的輸入，來創造幾何感知的貼圖效果。
helpx_creative_field: ""
helpx_description: Painter > Content > Creating custom effects > Mesh Based Input
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 基於網格的輸入
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 0%

---


# 基於網格的輸入

基於網格的輸入是由 Substance 3D Painter 引擎從目前專案中的網格中擷取的貼圖。 這些貼圖可以用來根據網格拓撲創造進階效果。

>[!NOTE]
>
> 這些網格資訊是基於拓撲本身，沒有考慮網格貼圖（烘焙的貼圖）。
> 
> 引擎提供的輸入是一個 32 位元浮點紋理，會被縮放/壓縮成 Substance 圖中輸入的值。

| 網狀資訊 | 識別碼 | 使用情況 | 說明 |
| --- | --- | --- | --- |
| *位置（RGB）* | **網狀_position** | **meshPosition** | 擷取包含頂點位置的貼圖。 |
| *世界太空標準（RGB）* | **網_world\_space\_normal** | **meshNormalWS** | 取得包含世界空間中頂點法線的貼圖。 |
| *世界空間切線（RGB）* | **網_world\_space\_tangent** | **meshTangentWS** | 擷取包含世界空間中頂點切線的貼圖。 |
| *世界太空雙切形（RGB）* | **網_world\_space\_bitangent** | **meshBitangentWS** | 取回包含世界空間中頂點雙切線（雙法線）的紋理。 |
| *像素尺寸（灰階）* | **網_texel\_size** | **meshTexelSize** | 取得包含紋素大小（像素密度與網格 UV 差異）的貼圖。 |
| *UV 遮罩（灰階）* | **網格\_uv\_mask** | **meshUVMask** | 取得一個貼圖，作為網格 UV 島的黑色（外部）和白色（內部）遮罩。 |
