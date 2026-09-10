---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/scripting-and-development/api-reference/shader-api/libraries-shader-api/lib-sparse-shader-api.html"
breadcrumb-title: ''
description: 取得 Substance 3D Painter 的 Lib Sparse shader API 參考，以便在自訂著色器中處理稀疏紋理取樣。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API > Libraries - Shader API > Lib Sparse - Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lib Sparse - Shader API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---


# Lib Sparse - Shader API

## lib-sparse.glsl

此檔案提供有用的功能，確保稀疏紋理取樣的正確性（ARB\_sparse\_texture）。 允許只取樣顯示記憶體中實際存在的部分紋理。

**Public Functions：** getSparseCoord **&#x200B; getSparseCoordLod0 &#x200B;** textureSparseQueryLod **&#x200B; textureSparse &#x200B;**

**公共結構：***SamplerSparse* *SparseCoord*

*只有啟用稀疏虛擬貼圖擴充功能時，FEATURE\_SPARSE\_TEXTURE* 巨集 才會被定義。

如果啟用了，請進行額外的材質查找檢查，以便在缺少 texel 時往上爬升 mipmap 金字塔。

```
## ifdef FEATURE_SPARSE_TEXTURE

//: param auto material_lod_check_needed 

uniform bool material_lod_check_needed = false; 

//: param auto material_lod_mask 

uniform usampler2D material_lod_mask; 

## endif // FEATURE_SPARSE_TEXTURE

//: param auto uvtile_reference_sampler 

uniform sampler2D uvtile_reference_sampler; 

//: param auto uvtile_size 

uniform vec2 uvtile_size; 

//: param auto uvtile_inverse_size 

uniform vec2 uvtile_inverse_size; 

//: param auto uvtile_lod_bias 

uniform float uvtile_lod_bias;
```


取樣器與稀疏貼圖資訊結構

用於查詢所有與取樣器相關的制服，並以單一自動綁定方式進行

```
struct SamplerSparse { 

  sampler2D tex; 

  vec4 size; // width, height, 1/width, 1/height 

  bool is_set; // a boolean indicating whether the texture is in the texture set or not 

  uvec3 lod_mask_select; // masking operations description allowing to retrieve loaded mipmaps information 

};
```


稀疏抽樣座標

儲存 UV 座標和材質層面稀疏的 LoD 遮罩

```
struct SparseCoord { 

  vec2 tex_coord; 

  vec2 dfdx; 

  vec2 dfdy; 

  float lod; 

  uint material_lod_mask; 

}; 

 

 

## if defined(SHADER_FRAGMENT)
```


建置紋理座標結構，由 *textureSparse（）* 取樣函式使用（必須從片段著色器呼叫）

範例： *SparseCoord uv1coord = getSparseCoord（inputs.multi\_tex\_coord[1]）;*

```
SparseCoord getSparseCoord(vec2 tex_coord) { 

  SparseCoord res; 

  res.tex_coord = tex_coord; 

  res.dfdx = dFdx(tex_coord); 

  res.dfdy = dFdy(tex_coord); 

## ifdef FEATURE_SPARSE_TEXTURE

  res.material_lod_mask = material_lod_check_needed ? 

    textureLod(material_lod_mask,tex_coord,0.0).r : 

    0u; 

  res.lod = getLodFromReferenceSampler(tex_coord); 

## endif // FEATURE_SPARSE_TEXTURE

  return res; 

} 

## endif
```


建置紋理座標結構，由 *textureSparse（）* 取樣函式所用 基礎層級取樣版本（若非片段著色器可用）

```
SparseCoord getSparseCoordLod0(vec2 tex_coord) { 

  SparseCoord res; 

  res.tex_coord = tex_coord; 

  res.dfdx = vec2(0.0); 

  res.dfdy = vec2(0.0); 

## ifdef FEATURE_SPARSE_TEXTURE

  res.material_lod_mask = material_lod_check_needed ? 

    textureLod(material_lod_mask,tex_coord,0.0).r : 

    0u; 

  res.lod = 0.0; 

## endif // FEATURE_SPARSE_TEXTURE

  return res; 

} 

 

## if defined(SHADER_FRAGMENT)
```


計算用來從稀疏紋理取樣的細節層級

如果缺少 texel，就往上爬 mipmap 金字塔，回傳 LoD 是在 LoD 偏誤施加前的

```
float textureSparseQueryLod(SamplerSparse sampler, SparseCoord coord) { 

## ifdef FEATURE_SPARSE_TEXTURE

  float lodfix = coord.lod; 

  if (material_lod_check_needed) { 

    lodfix = getFixedSparseLod(getTextureLodMask(sampler.lod_mask_select, coord.material_lod_mask), lodfix); 

  } 

  return lodfix-uvtile_lod_bias; 

## else // FEATURE_SPARSE_TEXTURE

  return textureQueryLod(sampler.tex, coord.tex_coord).y-uvtile_lod_bias; 

## endif // FEATURE_SPARSE_TEXTURE

} 

## endif // SHADER_FRAGMENT
```


計算用來從稀疏紋理取樣的導數

如果缺少 texel，就往上爬 mipmap 金字塔

```
void textureSparseQueryGrad(out vec2 dfdx, out vec2 dfdy, SamplerSparse sampler, SparseCoord coord) { 

## ifdef FEATURE_SPARSE_TEXTURE

  if (material_lod_check_needed) { 

    float lodfix = getFixedSparseLod(getTextureLodMask(sampler.lod_mask_select, coord.material_lod_mask), coord.lod); 

    if (coord.lod!=lodfix) { 

      // Fix dfdx dfdy, take account offset, no more anisotropy 

      vec2 ddfix = exp2(lodfix-uvtile_lod_bias) * uvtile_inverse_size; 

      dfdx = vec2(ddfix.x,0.0); 

      dfdy = vec2(0.0,ddfix.y); 

      return; 

    } 

  } 

## endif // FEATURE_SPARSE_TEXTURE

  dfdx = coord.dfdx; 

  dfdy = coord.dfdy; 

}
```


對稀疏貼圖做貼圖查找，必要時再往上看 mipmap 層級

此函式取代標準 *紋理（sampler2D， vec2），* 用以從稀疏紋理中擷取像素

```
vec4 textureSparse(SamplerSparse sampler, SparseCoord coord) { 

  vec2 dfdx,dfdy; 

  textureSparseQueryGrad(dfdx, dfdy, sampler, coord); 

  return textureGrad(sampler.tex, coord.tex_coord, dfdx, dfdy); 

}
```


給定一個貼圖，會以小偏移量進行多次優化的貼圖查找

我們提供此輔助工具的替代版本，最高可達 N=4

```
void textureSparseOffsets(SamplerSparse sampler, SparseCoord coord, vec2 offsets[N], out vec4 results[N]) { 

  vec2 dfdx,dfdy; 

  textureSparseQueryGrad(dfdx, dfdy, sampler, coord); 

  for(int i = 0; i < N; ++i) { 

    results[i] = textureGrad(sampler.tex, coord.tex_coord + offsets[i], dfdx, dfdy); 

  } 

} 

 
```
