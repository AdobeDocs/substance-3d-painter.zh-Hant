---
breadcrumb-title: ""
description: 請取得 Lib Bayer 著色器 API 參考，以 Substance 3D Painter 在自訂著色器中建立 Bayer 抖動圖案。
title: Lib Bayer - Shader API
user-guide-description: ""
user-guide-title: ""
source-git-commit: 6b6d52207ca1d043aaa1b2b14145b6b49d4c1942
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
