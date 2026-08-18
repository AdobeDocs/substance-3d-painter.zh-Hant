---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/scripting-and-development/api-reference/shader-api/libraries-shader-api/lib-emissive-shader-api.html"
breadcrumb-title: ''
description: 存取 Substance 3D Painter 的 Lib Emissive shader API 參考，以創建發光材質與發光效果。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API > Libraries - Shader API > Lib Emissive - Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lib Emissive - Shader API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 0%

---


# Lib Emissive - Shader API

## lib-emissive.glsl

**公共函數：***pbrComputeEmissive*

從函式庫匯入

```
import lib-sparse.glsl
```


發射通道紋理。

```
//: param auto channel_emissive 

uniform SamplerSparse emissive_tex;
```


用來調整發射強度的數值。

```
//: param custom { 

//:   "default": 1.0, 

//:   "label": "Emissive Intensity", 

//:   "min": 0.0, 

//:   "max": 100.0, 

//:   "group": "Common Parameters" 

//: } 

uniform float emissive_intensity;
```


計算觀察者眼睛的發射輻射度

```
vec3 pbrComputeEmissive(SamplerSparse emissive, SparseCoord coord) 

{ 

  return emissive_intensity * textureSparse(emissive, coord).rgb; 

} 

 
```
