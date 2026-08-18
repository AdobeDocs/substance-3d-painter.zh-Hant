---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/scripting-and-development/api-reference/shader-api/shaders-shader-api/pixelated-shader-api.html"
breadcrumb-title: ''
description: 存取 Substance 3D Painter 的 Pixelated shader API 參考，以創建自訂的像素渲染效果。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API > Shaders - Shader API > Pixelated - Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Pixelated - 著色器 API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---


# Pixelated - 著色器 API

## 基本的像素化著色器

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


**優先** 順序是進行 **輪廓檢測**。 若輪廓條件達到，則以黑色退出。

```
  if (NdV < mix(unlit_outline_thickness, lit_outline_thickness, NdL)) { 

    return; 

  } 

 

  vec3 baseColor = getBaseColor(basecolor_tex, inputs.sparse_coord);
```


根據底色亮度，對遮罩尺寸引入一些抖動

```
  float maskRadiusJitter = pow(dot(baseColor, vec3(0.3333)), 0.1);
```


根據片段的螢幕空間位置計算遮罩值。 這樣會形成一個格狀的圖案。

```
  float mask = pow(1.0 - length(fract(gl_FragCoord.xy / 7.0) - vec2(0.5)), maskRadiusJitter * 5.0) * 5.0;
```


這裡，我們取樣基色並施加簡單的漫反射衰減

```
  vec3 color = baseColor * NdL; 

 

  diffuseShadingOutput(mask * color); 

} 

 
```
