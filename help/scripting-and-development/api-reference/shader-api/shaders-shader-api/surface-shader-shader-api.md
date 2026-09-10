---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/scripting-and-development/api-reference/shader-api/shaders-shader-api/surface-shader-shader-api.html"
breadcrumb-title: ''
description: 存取 Substance 3D Painter 的 Surface Shader API 參考，以創建自訂的表面著色器效果與材質。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API > Shaders - Shader API > Surface Shader - Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Surface Shader - Shader API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---


# Surface Shader - Shader API

## surface-shader.glsl

要建立可在 Substance Painter 中使用的著色器資源，只需建立一個包含單一函 *式 shade* 的 glsl 檔案，設定檔如下：

```
void shade(V2F inputs);
```


## V2F 輸入類型定義：

```
struct V2F { 

  vec3 normal;               // interpolated normal 

  vec3 tangent;              // interpolated tangent 

  vec3 bitangent;            // interpolated bitangent 

  vec3 position;             // interpolated position 

  vec4 color[1];             // interpolated vertex colors (color0) 

  vec2 tex_coord;            // interpolated texture coordinates (uv0) 

  SparseCoord sparse_coord;  // interpolated sparse texture coordinates used by textureSparse() sampling function 

  vec2 multi_tex_coord[8];   // interpolated texture coordinates (uv0-uv7) 

};
```


注意：要取得 uv1-uv7 的 SparseCoord，必須明確呼叫 *getSparseCoord（vec2），* 定義於 [lib-sparse.glsl](../libraries-shader-api/lib-sparse-shader-api.md)

## 表面著色器輸出：

以下函式可從 *著色* 函式中呼叫來描述片段屬性：

```
// fragment opacity. default value: 1.0 

void alphaOutput(float); 

// diffuse lighting contribution. default value: vec3(0.0) 

void diffuseShadingOutput(vec3); 

// specular lighting contribution. default value: vec3(0.0) 

void specularShadingOutput(vec3); 

// color emitted by the fragment. default value: vec3(0.0) 

void emissiveColorOutput(vec3); 

// fragment color. default value: vec3(1.0) 

void albedoOutput(vec3); 

// subsurface scattering properties, see lib-sss.glsl for details. default value: vec4(0.0) 

void sssCoefficientsOutput(vec4);
```


舉例來說，計算片段顏色最基本的渲染方程式為： *emissiveColor + 反照率 \* 漫反射陰影 + 高光陰影*
