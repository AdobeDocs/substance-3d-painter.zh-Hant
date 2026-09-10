---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/scripting-and-development/api-reference/shader-api/libraries-shader-api/lib-normal-shader-api.html"
breadcrumb-title: ''
description: 存取 Substance 3D Painter 的 Lib Normal shader API 參考，以便在自訂著色器中處理法線貼圖和表面法線。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API > Libraries - Shader API > Lib Normal - Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lib Normal - 著色器 API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---


# Lib Normal - 著色器 API

## lib-normal.glsl

**公開函式：**&#x200B;正常 混合&#x200B;**&#x200B;正常 混合 定向 &#x200B;** 正常&#x200B;**&#x200B;解包&#x200B;**&#x200B;從基礎 正常 **&#x200B; 正常 從正常&#x200B;**&#x200B;正常 從高度&#x200B;**&#x200B;取得 TSNormal &#x200B;**&#x200B;計算WSBase 正常&#x200B;**&#x200B;計算WSNormal &#x200B;**

從函式庫匯入

```
import lib-defines.glsl 

import lib-sparse.glsl
```


所有引擎參數皆適用於正常中心操作。

```
//: param auto channel_height 

uniform SamplerSparse height_texture; 

//: param auto channel_normal 

uniform SamplerSparse normal_texture; 

//: param auto texture_normal 

uniform SamplerSparse base_normal_texture; 

//: param auto normal_blending_mode 

uniform int normal_blending_mode;
```


用於反轉法線貼圖的 Y 軸

```
//: param auto normal_y_coeff 

uniform float base_normal_y_coeff;
```


由我們的藝術家經驗決定......

```
const float HEIGHT_FACTOR = 400.0;
```


對兩個法線貼圖進行混合

這是基於白粉混合 http://blog.selfshadow.com/publications/blending-in-detail/

```
vec3 normalBlend(vec3 baseNormal, vec3 overNormal) 

{ 

  return normalize(vec3( 

    baseNormal.xy + overNormal.xy, 

    baseNormal.z  * overNormal.z)); 

}
```


在兩個法線貼圖之間進行細節導向的混合

這是基於細節導向的混合 http://blog.selfshadow.com/publications/blending-in-detail/

```
vec3 normalBlendOriented(vec3 baseNormal, vec3 overNormal) 

{ 

  baseNormal.z += 1.0; 

  overNormal.xy = -overNormal.xy; 

  return normalize(baseNormal * dot(baseNormal,overNormal) - 

    overNormal*baseNormal.z); 

}
```


回傳一個被衰減因子壓平的正規值

```
vec3 normalFade(vec3 normal,float attenuation) 

{ 

  if (attenuation<1.0 && normal.z<1.0) 

  { 

    float phi = attenuation * acos(normal.z); 

    normal.xy *= 1.0/sqrt(1.0-normal.z*normal.z) * sin(phi); 

    normal.z = cos(phi); 

  } 

 

  return normal; 

}
```


拆解一個普通的 alpha 通道

```
vec3 normalUnpack(vec4 normal_alpha, float y_coeff) 

{ 

  if (normal_alpha.a == 0.0 || normal_alpha.xyz == vec3(0.0)) { 

    return vec3(0.0, 0.0, 1.0); 

  } 

 

  // Attenuation in function of alpha 

  vec3 normal = normal_alpha.xyz/normal_alpha.a * 2.0 - vec3(1.0); 

  normal.y *= y_coeff; 

  normal.z = max(1e-3, normal.z); 

  normal = normalize(normal); 

  normal = normalFade(normal, normal_alpha.a); 

 

  return normal; 

}
```


拆包一個正常的帶 alpha 通道，沒有 Y 反轉

```
vec3 normalUnpack(vec4 normal_alpha) 

{ 

  return normalUnpack(normal_alpha, 1.0); 

}
```


從文件的高度通道計算法線切空間

```
vec3 normalFromHeight(SparseCoord coord, float height_force) 

{ 

  // Normal computation using height map 

 

  // Determine gradient offset in function of derivatives 

  vec2 dfd = max(coord.dfdx,coord.dfdy); 

  dfd = max(dfd,height_texture.size.zw); 

 

  vec2 dfdx,dfdy; 

  textureSparseQueryGrad(dfdx, dfdy, height_texture, coord); 

  float h_r  = textureGrad(height_texture.tex, coord.tex_coord+vec2( dfd.x,  0    ), dfdx, dfdy).r; 

  float h_l  = textureGrad(height_texture.tex, coord.tex_coord+vec2(-dfd.x,  0    ), dfdx, dfdy).r; 

  float h_t  = textureGrad(height_texture.tex, coord.tex_coord+vec2(     0,  dfd.y), dfdx, dfdy).r; 

  float h_b  = textureGrad(height_texture.tex, coord.tex_coord+vec2(     0, -dfd.y), dfdx, dfdy).r; 

  float h_rt = textureGrad(height_texture.tex, coord.tex_coord+vec2( dfd.x,  dfd.y), dfdx, dfdy).r; 

  float h_lt = textureGrad(height_texture.tex, coord.tex_coord+vec2(-dfd.x,  dfd.y), dfdx, dfdy).r; 

  float h_rb = textureGrad(height_texture.tex, coord.tex_coord+vec2( dfd.x, -dfd.y), dfdx, dfdy).r; 

  float h_lb = textureGrad(height_texture.tex, coord.tex_coord+vec2(-dfd.x, -dfd.y), dfdx, dfdy).r; 

 

  vec2 dh_dudv = (0.5 * height_force) / dfd * vec2( 

    2.0*(h_l-h_r)+h_lt-h_rt+h_lb-h_rb, 

    2.0*(h_b-h_t)+h_rb-h_rt+h_lb-h_lt); 

 

  return normalize(vec3(dh_dudv, HEIGHT_FACTOR)); 

}
```


輔助工具用來計算切空間法線與基底法線、高度值，以及可選的細節法線。

```
vec3 getTSNormal(SparseCoord coord, vec3 normalFromHeight) 

{ 

  vec3 normal = normalBlendOriented( 

    normalUnpack(textureSparse(base_normal_texture, coord), base_normal_y_coeff), 

    normalFromHeight); 

 

  if (normal_texture.is_set) { 

    vec3 channelNormal = normalUnpack(textureSparse(normal_texture, coord)); 

    if (normal_blending_mode == BlendingMode_Replace) { 

      normal = normalBlendOriented(normalFromHeight, channelNormal); 

    } else if (normal_blending_mode == BlendingMode_NM_Combine) { 

      normal = normalBlendOriented(normal, channelNormal); 

    } 

  } 

 

  return normal; 

}
```


輔助工具用來計算從基底法線和高度計算切線空間法線，並可選地提供細節法線。

```
vec3 getTSNormal(SparseCoord coord) 

{ 

  float height_force = 1.0; 

  vec3 normalH = normalFromHeight(coord, height_force); 

  return getTSNormal(coord, normalH); 

}
```


輔助工具可從切空間基準法線計算世界空間法線。

```
vec3 computeWSBaseNormal(SparseCoord coord, vec3 tangent, vec3 bitangent, vec3 normal) 

{ 

  vec3 normal_vec = normalUnpack(textureSparse(normal_texture, coord), base_normal_y_coeff); 

  return normalize( 

    normal_vec.x * tangent + 

    normal_vec.y * bitangent + 

    normal_vec.z * normal 

  ); 

}
```


輔助工具用來計算由 getTSNormal 輔助工具提供的切向空間法線，以及網格的局部框架。

```
vec3 computeWSNormal(SparseCoord coord, vec3 tangent, vec3 bitangent, vec3 normal) 

{ 

  vec3 normal_vec = getTSNormal(coord); 

  return normalize( 

    normal_vec.x * tangent + 

    normal_vec.y * bitangent + 

    normal_vec.z * normal 

  ); 

} 

 
```
