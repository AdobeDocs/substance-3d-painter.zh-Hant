---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/scripting-and-development/api-reference/shader-api/libraries-shader-api/lib-random-shader-api.html"
breadcrumb-title: ''
description: 存取 Substance 3D Painter 的 Lib Random shader API 參考，以便在自訂著色器開發中產生隨機值。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API > Libraries - Shader API > Lib Random - Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lib Random - 著色器 API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# Lib Random - 著色器 API

## lib-random.glsl

**公共函數：** getBlueNoiseThreshold **&#x200B; getBlueNoiseThreshold temporal &#x200B;** fibonacci1D **&#x200B; fibonacci2D &#x200B;** fibonacci2D itheredTemporal **

從函式庫匯入

```
import lib-defines.glsl
```


包含純量值的二維藍噪紋理

```
//: param auto texture_blue_noise 

uniform sampler2D texture_blue_noise;
```


藍噪紋理解析度

```
const ivec2 texture_blue_noise_size = ivec2(256);
```


目前影格隨機種子

```
//: param auto random_seed 

uniform int alg_random_seed;
```


根據像素座標取得均勻的隨機值。

```
float getBlueNoiseThreshold() 

{ 

  return texture(texture_blue_noise, gl_FragCoord.xy / vec2(texture_blue_noise_size)).x + 0.5 / 65536.0; 

}
```


根據像素座標和幀識別碼，取得一個均勻的隨機值。

```
float getBlueNoiseThresholdTemporal() 

{ 

  return fract(getBlueNoiseThreshold() + M_GOLDEN_RATIO * alg_random_seed); 

}
```


從斐波那契數列返回第i **&#x200B;個數字。

```
float fibonacci1D(int i) 

{ 

  return fract((float(i) + 1.0) * M_GOLDEN_RATIO); 

}
```


返回費波那契數列中的第&#x200B;*i*&#x200B;對。nbSample 是獲得均勻分布的必要條件。

```
vec2 fibonacci2D(int i, int nbSamples) 

{ 

  return vec2( 

    (float(i)+0.5) / float(nbSamples), 

    fibonacci1D(i) 

  ); 

}
```


返回費波那契數列中的第&#x200B;*i*&#x200B;對。nbSample 是獲得均勻分布的必要條件。 此版本採用每幀及每像素的偽隨機旋轉。

```
vec2 fibonacci2DDitheredTemporal(int i, int nbSamples) 

{ 

  vec2 s = fibonacci2D(i, nbSamples); 

  s.x += getBlueNoiseThresholdTemporal(); 

  return s; 

} 

 
```
