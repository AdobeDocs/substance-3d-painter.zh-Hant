---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/scripting-and-development/api-reference/shader-api/shaders-shader-api/toon-shader-api.html"
breadcrumb-title: ''
description: 取得 Substance 3D Painter 的 Toon 著色器 API 參考，以創造自訂的卡通風格渲染效果。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API > Shaders - Shader API > Toon - Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Toon - 著色器 API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---


# Toon - 著色器 API

## 基本的卡通著色器

從函式庫匯入。

```
import lib-sampler.glsl
```


我們定義全域光源位置

```
const vec3 light_pos = vec3(10.0, 10.0, 10.0);
```


我們將 **自動參數的世界視角綁定** 到統一 **的相機_pos**。

```
//: param auto world_eye_position 

uniform vec3 camera_pos;
```


我們將&#x200B;**文件的通道**&#x200B;基底顏色&#x200B;**綁定**&#x200B;到統一&#x200B;**基色\_tex**。

```
//: param auto channel_basecolor 

uniform SamplerSparse basecolor_tex;
```


我們&#x200B;**會將網格曲率綁定****到均勻**&#x200B;曲率_tex ****。若無法提供曲率，則提供透明紋理。

```
//: param auto texture_curvature 

uniform SamplerSparse curvature_tex;
```


我們為這個著色器定義了一個新的自訂調整，並附上它的預設值。 這個用來調整陰影時輪廓的粗細。

```
//: param custom { 

//:  "default": 0.4, 

//:   "min": 0.0, 

//:   "max": 1.0, 

//:   "label": "Unlit outline thickness" 

//: } 

uniform float unlit_outline_thickness;
```


我們為這個著色器定義了一個新的自訂調整，並附上它的預設值。 這個用來調整點亮時輪廓的粗細。

```
//: param custom { 

//:   "default": 0.1, 

//:   "min": 0.0, 

//:   "max": 1.0, 

//:   "label": "Lit outline thickness" 

//: } 

uniform float lit_outline_thickness;
```


不管我們是否偏好使用曲率。

```
//: param custom { 

//:   "default": false, 

//:   "label": "Use curvature" 

//: } 

uniform bool use_curvature;
```


著色器的入口點。

```
void shade(V2F inputs) 

{
```


我們計算出幾個有用的數值。

```
  vec3 V = normalize(camera_pos - inputs.position); 

  vec3 N = normalize(inputs.normal); 

  vec3 L = normalize(light_pos - inputs.position); 

  float NdV = dot(N, V); 

  float NdL = max(0.0, dot(N, L));
```


**優先** 順序是進行 **輪廓檢測**。 讓使用者自行選擇是否偏好使用曲率地圖來偵測輪廓。

```
  if (use_curvature) { 

    float curv = textureSparse(curvature_tex, inputs.sparse_coord).r; 

    NdV = 1.0 - curv; 

  }
```


若輪廓條件達到，則以黑色退出。

```
  if (NdV < mix(unlit_outline_thickness, lit_outline_thickness, NdL)) { 

    return; 

  }
```


在這裡，我們進行四個步驟的色彩離散化。

```
  vec3 color = getBaseColor(basecolor_tex, inputs.sparse_coord); 

  if (NdL > 0.75) { 

    color = color; 

  } else if (NdL > 0.5) { 

    color = color * 0.5; 

  } else if (NdL > 0.1) { 

    color = color * 0.1; 

  } 

  else
```


備用是黑色。

```
    color = vec3(0.0); 

 

  diffuseShadingOutput(color); 

} 

 
```
