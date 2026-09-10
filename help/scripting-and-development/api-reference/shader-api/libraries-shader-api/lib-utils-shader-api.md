---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/scripting-and-development/api-reference/shader-api/libraries-shader-api/lib-utils-shader-api.html"
breadcrumb-title: ''
description: 存取 Substance 3D Painter 的 Lib Utils shader API 參考，以便在自訂著色器開發中使用工具函式。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API > Libraries - Shader API > Lib Utils - Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lib Utils - Shader API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---


# Lib Utils - Shader API

## 寓言效用函數

## 色調對應

這些是你可以在著色器中使用的色調映射範例。 Painter 除了 Yebis 可選的那個外，沒有套用任何音調映射。 如果你決定在著色器裡做一些色調映射，它會先套用在 Yebis 色調映射之前。

根據參數 sigma 和 n 執行 S 曲線音調映射。

```
vec3 tonemapSCurve(vec3 value, float sigma, float n) 

{ 

  vec3 pow_value = pow(value, vec3(n)); 

  return pow_value / (pow_value + pow(sigma, n)); 

}
```


## sRGB 轉換

這些就是 Painter 所使用的轉換。 你可以在視口中自動覆蓋線性 -> sRGB 轉換，方法是將這條線放入自訂著色器中：

*#define 失效_FRAMEBUFFER\_SRGB_CONVERSION*

還有自己做客製化轉換。

sRGB 轉線性色彩轉換。 標量版本。

```
float sRGB2linear(float x) 

{ 

  return x <= 0.04045 ? 

    x * 0.0773993808 : // 1.0/12.92 

    pow((x + 0.055) / 1.055, 2.4); 

}
```


sRGB 轉線性色彩轉換。 RGB 版本。

```
vec3 sRGB2linear(vec3 rgb) 

{ 

  return vec3( 

    sRGB2linear(rgb.r), 

    sRGB2linear(rgb.g), 

    sRGB2linear(rgb.b)); 

}
```


sRGB 轉線性色彩轉換。 RGB + Alpha 版本。

```
vec4 sRGB2linear(vec4 rgba) 

{ 

  return vec4(sRGB2linear(rgba.rgb), rgba.a); 

}
```


線性轉 sRGB 色彩轉換。 標量版本。

```
float linear2sRGB(float x) 

{ 

  return x <= 0.0031308 ? 

      12.92 * x : 

      1.055 * pow(x, 0.41666) - 0.055; 

}
```


線性轉 sRGB 色彩轉換。 RGB 版本。

```
vec3 linear2sRGB(vec3 rgb) 

{ 

  return vec3( 

      linear2sRGB(rgb.r), 

      linear2sRGB(rgb.g), 

      linear2sRGB(rgb.b)); 

}
```


線性轉 sRGB 色彩轉換。 RGB + Alpha 版本。

```
vec4 linear2sRGB(vec4 rgba) 

{ 

  return vec4(linear2sRGB(rgba.rgb), rgba.a); 

}
```


線性轉為 sRGB 色彩轉換可選。 標量版本。

```
//: param auto conversion_linear_to_srgb 

uniform bool convert_to_srgb_opt; 

float linear2sRGBOpt(float x) 

{ 

  return convert_to_srgb_opt ? linear2sRGB(x) : x; 

}
```


線性轉為 sRGB 色彩轉換可選。 RGB 版本。

```
vec3 linear2sRGBOpt(vec3 rgb) 

{ 

  return convert_to_srgb_opt ? linear2sRGB(rgb) : rgb; 

}
```


線性轉為 sRGB 色彩轉換可選。 RGB + Alpha 版本。

```
vec4 linear2sRGBOpt(vec4 rgba) 

{ 

  return convert_to_srgb_opt ? linear2sRGB(rgba) : rgba; 

}
```


顏色轉換。 標量版本。

```
uniform int output_conversion_method; 

float convertOutput(float x) 

{ 

 if (output_conversion_method == 0) return x; 

 else if (output_conversion_method == 1) return linear2sRGB(x); 

 else return sRGB2linear(x); 

}
```


顏色轉換。 RGB 版本。

```
vec3 convertOutput(vec3 rgb) 

{ 

 if (output_conversion_method == 0) return rgb; 

 else if (output_conversion_method == 1) return linear2sRGB(rgb); 

 else return sRGB2linear(rgb); 

}
```


顏色轉換。 RGB + Alpha 版本。

```
vec4 convertOutput(vec4 rgba) 

{ 

 if (output_conversion_method == 0) return rgba; 

 else if (output_conversion_method == 1) return linear2sRGB(rgba); 

 else return sRGB2linear(rgba); 

}
```


## 抖動

這些是幫忙在著色器中添加抖動的輔助工具。

抖動模式使用 8x8 拜耳矩陣

```
import lib-bayer.glsl 

 

float getDitherThreshold(uvec2 coords) 

{ 

  return bayerMatrix8(coords); 

} 

 

 

vec4 RGB2Gray(vec4 rgba) 

{ 

  float gray = 0.299 * rgba.r + 0.587 * rgba.g + 0.114 * rgba.b; 

  return vec4(vec3(gray), rgba.a); 

}
```


移除光面金屬表面（靠近鏡子）的 AO 和陰影

```
float specularOcclusionCorrection(float diffuseOcclusion, float metallic, float roughness) 

{ 

  return mix(diffuseOcclusion, 1.0, metallic * (1.0 - roughness) * (1.0 - roughness)); 

} 

 
```
