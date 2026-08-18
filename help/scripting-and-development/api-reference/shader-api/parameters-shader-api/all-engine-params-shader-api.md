---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/scripting-and-development/api-reference/shader-api/parameters-shader-api/all-engine-params-shader-api.html"
breadcrumb-title: ''
description: 存取 Substance 3D Painter 的 All Engine Params shader API 參考，以控制引擎層級的著色器參數。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API > Parameters - Shader API > All Engine Params - Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 所有引擎參數 - 著色器 API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---


# 所有引擎參數 - 著色器 API

## 引擎參數範例

## 貼圖參數

Substance Painter 使用稀疏虛擬貼圖（SVT）系統來在視窗中顯示貼圖。

欲了解更多系統資訊，請參閱 [線上文件](../../../../features/sparse-virtual-textures.md)。

這個系統對著色器程式碼的撰寫方式有影響。 我們提供協助工具，透過 SamplerSparse *結構與紋理查找函式（參見 [lib-sparse.glsl](../libraries-shader-api/lib-sparse-shader-api.md)）簡化使用*。

基本用法：

```
// Defines the SamplerSparse structure 

import lib-sparse.glsl 

 

//: param auto TEXTURE_TAG 

uniform SamplerSparse uniform_tex;   // Texture sampler and its information
```


貼圖參數允許使用 &#39;or&#39; 運算子來定義備援：

```
//: param auto TEXTURE_TAG_1 or TEXTURE_TAG_2 

uniform SamplerSparse uniform_tex; // if TEXTURE_TAG_1 exists then TEXTURE_TAG_1 else TEXTURE_TAG_2
```


其中 *TEXTURE\_TAG* 是下面描述的標籤之一。

### 文件的通道標籤

所有這些紋理都預先 **放大** 並 **膨** 脹，以避免接縫問題。

**貼圖集通道**

*頻道\_ambientocclusion*&#x200B;頻道\_anisotropyangle **&#x200B;頻道\_anisotropylevel頻道\_basecolor **&#x200B;頻道\_blendingmask ****&#x200B;頻道\_diffuse **&#x200B;頻道\_displacement **&#x200B;頻道\_emissive **&#x200B;頻道\_glossiness **&#x200B;頻道\_height_ior ****&#x200B;頻道\頻道\_metallic **&#x200B;頻道\_normal **&#x200B;頻道\_opacity頻道\_reflection **** *頻道\_roughness**頻道\_scattering**頻道\_specular**頻道\_specularlevel**頻道\_transmissive*

**使用者頻道**

*頻道\_user0**頻道\_user1**頻道\_user2**頻道\_user3**頻道\_user4**頻道\_user5**頻道\_user6**頻道\_user7*

### 網格貼圖

*texture\_ambientocclusion* ：環境遮蔽貼圖\
*texture\_curvature* ：曲率貼圖\
*texture\_id* ： ID map\
*texture\_normal* ：切線空間法線貼圖\
*texture\_normal\_ws* ：世界空間法線貼圖\
*紋理\_position* ：世界空間位置圖\
*材質\_thickness* ：厚度貼圖

## 額外材質參數

基本用法：

```
//: param auto TEXTURE_TAG 

uniform sampler2D uniform_tex;   // The texture itself 

 

//: param auto TEXTURE_TAG_size 

uniform vec4 uniform_tex_size;   // The size of the texture (width, height, 1/width, 1/height)
```


貼圖參數允許使用 &#39;or&#39; 運算子來定義備援：

```
//: param auto TEXTURE_TAG_1 or TEXTURE_TAG_2 

uniform sampler2D uniform_tex; // if TEXTURE_TAG_1 exists then TEXTURE_TAG_1 else TEXTURE_TAG_2 

 

//: param auto TEX_TAG_1_size or TEX_TAG_2_size 

uniform vec4 uniform_tex_size; // if TEX_TAG_1 exists then TEX_TAG_1_size else TEX_TAG_2_size
```


其中 *TEXTURE\_TAG* 是下面描述的標籤之一。

*質感\_blue\_noise* ：藍噪紋理\
*texture\_environment* ：環境貼圖， **mip-mapped，**&#x200B;使用 [lib-env.glsl](../libraries-shader-api/lib-env-shader-api.md) 來使用這個

## 其他參數

*aspect\_ratio* ：包含視窗&#x200B;*寬度與高度*&#x200B;比值的浮點&#x200B;**&#x200B;點數

```
//: param auto aspect_ratio 

uniform float uniform_aspect_ratio;
```


*Camera\_view\_matrix*：*一個代表從世界空間到相機空間的MAT4*

```
//: param auto camera_view_matrix 

uniform mat4 uniform_camera_view_matrix;
```


*攝影機\_view\_matrix\_it* ：攝影機的反轉調版本 *\_view\_matrix*

```
//: param auto camera_view_matrix_it 

uniform mat4 uniform_camera_view_matrix_it;
```


*攝影機\_vp\_matrix\_inverse* ：投影的 *反演 \* 攝影機\_view\_matrix* 矩陣

```
//: param auto camera_vp_matrix_inverse 

uniform mat4 uniform_camera_vp_matrix_inverse;
```


*environment\_exposure* ：*一個代表環境圖曝光的浮點*

```
//: param auto environment_exposure 

uniform float uniform_environment_exposure;
```


*環境\_max\_lod* ： *一個浮點* ，代表 ENVMAP 在 MIP-Map 金字塔的深度

```
//: param auto environment_max_lod 

uniform float uniform_max_lod;
```


*environment\_rotation* ：一個&#x200B;*浮點，代表 envmap 繞上軸旋轉的過程*\
該值位於範圍 [0,1]，並應映射到 [0， 2\*pi] 範圍。

```
//: param auto environment_rotation 

uniform float uniform_environment_rotation;
```


*faceing* ： *表示渲染面的整* 數（-1：背面面，0：未定義面，1：正面面）\
值為 0 表示你可以放心依賴 GLSL 內建的變數 *GL\_FrontFacing*

```
//: param auto facing 

uniform int uniform_facing;
```


*fovy*：*代表相機沿Y軸視野的浮點*

```
//: param auto fovy 

uniform float uniform_fovy;
```


*is\_2d\_view* ：一個 *布爾* ，表示渲染是否為2D視圖進行

```
//: param auto is_2d_view 

uniform bool uniform_2d_view;
```


*是\_perspective\_projection* ：一個 *布ol* ，表示投影是透視還是正交投影

```
//: param auto is_perspective_projection 

uniform bool uniform_perspective_projection;
```


*主燈\_light* ：一個 *VEC4* ，表示主燈在環境中的位置

```
//: param auto main_light 

uniform vec4 uniform_main_light;
```


*MVP\_matrix*：一個&#x200B;*代表模型視圖投影矩陣的 MAT4*

```
//: param auto mvp_matrix 

uniform mat4 uniform_mvp_matrix;
```


*scene\_original\_radius* ：一個 *浮點* ，代表場景包圍球體在正規化前的半徑

```
//: param auto scene_original_radius 

uniform float uniform_scene_original_radius;
```


*Screen\_size*：*包含螢幕尺寸資料*（寬度、高度、1/寬度、1/高度）的 VEC4 **

```
//: param auto screen_size 

uniform vec4 uniform_screen_size;
```


*世界\_camera\_direction*：一台&#x200B;*代表世界相機方向的VEC3*

```
//: param auto world_camera_direction 

uniform vec3 uniform_world_camera_direction;
```


*世界\_eye\_position*：*一個代表世界視眼位置的VEC3*

```
//: param auto world_eye_position 

uniform vec3 uniform_world_eye_position; 

 
```
