---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/scripting-and-development/api-reference/shader-api/libraries-shader-api/lib-alpha-shader-api.html"
breadcrumb-title: ''
description: 存取 Lib Alpha 著色器 API 參考，以支援 Substance 3D Painter 中的 Alpha 通道與透明度，用於自訂著色器中。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API > Libraries - Shader API > Lib Alpha - Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lib Alpha - 著色器 API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 0%

---


# Lib Alpha - 著色器 API

## lib-alpha.glsl

**公開活動：***alphaKill*

```
import lib-sampler.glsl 

import lib-random.glsl
```


不透明度地圖，由引擎提供。

```
//: param auto channel_opacity 

uniform SamplerSparse opacity_tex;
```


Alpha測試門檻。

```
//: param custom { 

//:   "default": 0.33, 

//:   "label": "Alpha threshold", 

//:   "min": 0.0, 

//:   "max": 1.0, 

//:   "group": "Common Parameters" 

//: } 

uniform float alpha_threshold;
```


Alpha 測試猶豫不決。

```
//: param custom { 

//:   "default": false, 

//:   "label": "Alpha dithering", 

//:   "group": "Common Parameters" 

//: } 

uniform bool alpha_dither;
```


模擬 alpha 測試：若當前片段的不透明度低於使用者定義的閾值，則丟棄該片段。 應該稱為 AFTER 紋理取樣呼叫：它可以破壞導數

```
void alphaKill(float alpha) 

{ 

  float threshold = alpha_dither ? getBlueNoiseThresholdTemporal() : alpha_threshold; 

  if (alpha < threshold) discard; 

} 

 

void alphaKill(SparseCoord coord) 

{ 

  alphaKill(getOpacity(opacity_tex, coord)); 

} 

 
```
