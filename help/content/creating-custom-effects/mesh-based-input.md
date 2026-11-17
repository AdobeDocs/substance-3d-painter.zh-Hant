---
breadcrumb-title: ""
description: 了解如何在 Substance 3D Painter 的自訂效果中使用基於網格的輸入，以創造具幾何感知的貼圖效果。
title: 基於網格的輸入
user-guide-description: ""
user-guide-title: ""
source-git-commit: 4432887b652896f77fc3c99010436ef44aeb8a3e
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%
---

# 基於網格的輸入

基於網格的輸入是由 Substance 3D Painter 引擎從目前專案中的網格中擷取出來的貼圖。 這些貼圖可以用來根據網格拓撲創造進階效果。

>[!NOTE]
>
> 這些網格資訊是基於拓撲本身，並未考慮網格貼圖（烘焙的貼圖）。
> 
> 引擎提供的輸入是一個 32 位元的浮點紋理，會被縮放/壓縮到與 Substance 圖中輸入值相符。

| 網格資訊 | 識別碼 | 使用情況 | 說明 |
| --- | --- | --- | --- |
| *位置（RGB）* | **網格\_position** | **meshPosition** | 擷取包含頂點位置的貼圖。 |
| *世界空間常態（RGB）* | **網格\_world\_space\_normal** | **meshNormalWS** | 擷取包含世界空間中頂點法線的貼圖。 |
| *世界空間切線（RGB）* | **網格\_world\_space\_tangent** | **meshTangentWS** | 擷取包含世界空間中頂點切線的貼圖。 |
| *世界空間雙切線（RGB）* | **網格\_world\_space\_bitangent** | **meshBitangentWS** | 擷取包含世界空間中頂點雙切線（雙法線）的貼圖。 |
| *紋素大小（灰階）* | **網格\_texel\_size** | **meshTexelSize** | 擷取包含紋理大小（像素密度與網格 UV 差異）的貼圖。 |
| *UV 遮色片（灰階）* | **網格\_uv\_mask** | **meshUVMask** | 擷取一個貼圖，作為網格 UV 島的黑色（外部）與白色（內部）遮罩。 |
| *UV 鄰居（RGB）* | **網格\_uv\_neighbor** | **meshUVNeighbor** | 擷取包含兩個資訊的材質。 UV 島內部儲存一般 UV 座標。 UV 島的外部儲存了 UV 接縫另一側像素的 UV 座標。 這種紋理可以用來創造無縫的效果。 |
