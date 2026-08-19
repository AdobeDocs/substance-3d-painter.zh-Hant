---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/scripting-and-development/api-reference/shader-api/parameters-shader-api/all-custom-params-shader-api.html"
breadcrumb-title: ''
description: 存取 Substance 3D Painter 的 All Custom Params shader API 參考，以定義並控制自訂著色器參數。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API > Parameters - Shader API > All Custom Params - Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 所有自訂參數 - 著色器 API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---


# 所有自訂參數 - 著色器 API

## 自訂參數取樣著色器

**請注意，所有自訂調整至少需要預設&#x200B;**&#x200B;值。**

透過加入 *群組* 值來分組參數。

在 UI 中隱藏參數，將可見&#x200B;*值設*&#x200B;為 *false* 。

透過設定 *描述* 值，為參數新增提示。

## 色彩參數

```
//: param custom { "default": 0, "label": "Color RGB", "widget": "color" } 

uniform vec3 u_color_float3; 

//: param custom { "default": 1, "label": "Color RGBA", "widget": "color" } 

uniform vec4 u_color_float4;
```


## 自旋盒參數

```
//: param custom { "default": 0, "label": "Int spinbox" } 

uniform int u_spin_int1; 

//: param custom { "default": 0, "label": "Int2 spinbox" } 

uniform ivec2 u_spin_int2; 

//: param custom { "default": 0, "label": "Int3 spinbox" } 

uniform ivec3 u_spin_int3; 

//: param custom { "default": 0, "label": "Int4 spinbox" } 

uniform ivec4 u_spin_int4; 

//: param custom { "default": 0, "label": "Float spinbox" } 

uniform float u_spin_float1; 

//: param custom { "default": 0, "label": "Float2 spinbox" } 

uniform vec2 u_spin_float2; 

//: param custom { "default": 0, "label": "Float3 spinbox" } 

uniform vec3 u_spin_float3; 

//: param custom { "default": 0, "label": "Float4 spinbox" } 

uniform vec4 u_spin_float4;
```


## 滑桿參數

```
//: param custom { "default": 0, "label": "Int slider", "min": 0, "max": 10 } 

uniform int u_slider_int1; 

//: param custom { "default": 0, "label": "Int slider", "min": 0, "max": 10, "step": 2 } 

uniform int u_slider_int1_stepped; 

//: param custom { "default": 0, "label": "Int2 slider", "min": 0, "max": 10 } 

uniform ivec2 u_slider_int2; 

//: param custom { "default": 0, "label": "Int3 slider", "min": 0, "max": 10 } 

uniform ivec3 u_slider_int3; 

//: param custom { "default": 0, "label": "Int4 slider", "min": 0, "max": 10 } 

uniform ivec4 u_slider_int4; 

//: param custom { "default": 0, "label": "Float slider", "min": 0.0, "max": 1.0 } 

uniform float u_slider_float1; 

//: param custom { "default": 0, "label": "Float2 slider", "min": 0.0, "max": 1.0 } 

uniform vec2 u_slider_float2; 

//: param custom { "default": [0.2, 0.5, 0.8], "label": "Float3 slider", "min": 0.0, "max": 1.0 } 

uniform vec3 u_slider_float3; 

//: param custom { "default": 0, "label": "Float4 slider", "min": 0.0, "max": 1.0, "step": 0.02 } 

uniform vec4 u_slider_float4_stepped;
```


## 布爾參數

```
//: param custom { "default": false, "label": "Boolean" } 

uniform bool u_bool;
```


## 取樣器參數

貼圖在書架中以名稱定義，必須屬於 *貼圖* 或 *環境* 類別。

```
//: param custom { "default": "", "default_color": [1.0, 1.0, 0.0, 1.0], "label": "Texture" } 

uniform sampler2D u_sampler1; 

//: param custom { "default": "texture_name", "label": "Texture" } 

uniform sampler2D u_sampler2; 

//: param custom { "default": "texture_name", "label": "Texture", "usage": "texture" } 

uniform sampler2D u_sampler3; 

//: param custom { "default": "texture_name", "label": "Texture", "usage": "environment" } 

uniform sampler2D u_sampler4;
```


## 組合盒參數

```
//: param custom { 

//:   "default": -1, 

//:   "label": "Combobox", 

//:   "widget": "combobox", 

//:   "values": { 

//:     "Value -1": -1, 

//:     "Value 0": 0, 

//:     "Value 10": 10 

//:   } 

//: } 

uniform int u_combobox;
```


著色器入口點

```
vec4 shade(V2F inputs) 

{ 

  // We simply return the value of the RGB color picker 

  return vec4(u_color_float3, 1.0); 

} 

 
```
