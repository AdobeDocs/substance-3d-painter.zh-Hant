---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/scripting-and-development/api-reference/shader-api/libraries-shader-api/lib-bayer-shader-api.html"
breadcrumb-title: ''
description: 請取得 Lib Bayer 著色器 API 參考，以 Substance 3D Painter 在自訂著色器中建立 Bayer 抖動圖案。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API > Libraries - Shader API > Lib Bayer - Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lib Bayer - Shader API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '32'
ht-degree: 0%

---


# Lib Bayer - Shader API

## lib-bayer.glsl

**公共功能：***拜耳矩陣8*

```
float bayerMatrix8(uvec2 coords) { 

  return (float(bayer(coords.x, coords.y)) + 0.5) / 64.0; 

} 

 
```
