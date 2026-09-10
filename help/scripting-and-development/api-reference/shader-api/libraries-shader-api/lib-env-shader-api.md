---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/scripting-and-development/api-reference/shader-api/libraries-shader-api/lib-env-shader-api.html"
breadcrumb-title: ''
description: 存取 Substance 3D Painter 的 Lib Env shader API 參考，以便在自訂著色器中處理環境貼圖與光照。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API > Libraries - Shader API > Lib Env - Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lib Env - Shader API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---


# Lib Env - Shader API

## lib-env.glsl

**Public Functions：** *envSampleLOD* *envIrradiance*

數學常數所需的資料

```
import lib-defines.glsl
```


引擎提供的參數

```
//: param auto texture_environment 

uniform sampler2D environment_texture; 

//: param auto environment_rotation 

uniform float environment_rotation; 

//: param auto environment_exposure 

uniform float environment_exposure; 

//: param auto environment_irrad_mat_red 

uniform mat4 irrad_mat_red; 

//: param auto environment_irrad_mat_green 

uniform mat4 irrad_mat_green; 

//: param auto environment_irrad_mat_blue 

uniform mat4 irrad_mat_blue;
```


幫助你體驗環境。 旋轉也被納入考量。 環境貼圖是幕後的全景環境圖，這也是為什麼需要從 Dir 向量額外計算的原因。

```
vec3 envSampleLOD(vec3 dir, float lod) 

{ 

  // WORKAROUND: Intel GLSL compiler for HD5000 is bugged on OSX: 

  // https://bugs.chromium.org/p/chromium/issues/detail?id=308366 

  // It is necessary to replace atan(y, -x) by atan(y, -1.0 * x) to force 

  // the second parameter to be interpreted as a float 

  vec2 pos = M_INV_PI * vec2(atan(-dir.z, -1.0 * dir.x), 2.0 * asin(dir.y)); 

  pos = 0.5 * pos + vec2(0.5); 

  pos.x += environment_rotation; 

  return textureLod(environment_texture, pos, lod).rgb * environment_exposure; 

}
```


回傳給定方向的輻照度。 計算基於環境的球面諧波投影。

```
vec3 envIrradiance(vec3 dir) 

{ 

  float rot = environment_rotation * M_2PI; 

  float crot = cos(rot); 

  float srot = sin(rot); 

  vec4 shDir = vec4(dir.xzy, 1.0); 

  shDir = vec4( 

    shDir.x * crot - shDir.y * srot, 

    shDir.x * srot + shDir.y * crot, 

    shDir.z, 

    1.0); 

  return max(vec3(0.0), vec3( 

      dot(shDir, irrad_mat_red * shDir), 

      dot(shDir, irrad_mat_green * shDir), 

      dot(shDir, irrad_mat_blue * shDir) 

    )) * environment_exposure; 

} 

 
```
