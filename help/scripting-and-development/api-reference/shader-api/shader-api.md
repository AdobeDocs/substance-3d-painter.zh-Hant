---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/scripting-and-development/api-reference/shader-api.html"
breadcrumb-title: ''
description: 存取 Substance 3D Painter 的 Shader API 參考，建立自訂著色器並擴充渲染功能。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 著色器 API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '702'
ht-degree: 0%

---


# 著色器 API

![](../../../assets/header-shader.jpg)

Substance Painter 使用著色器在即時視口中渲染材質。 也可以寫自訂著色器來實作新行為，或讓視埠匹配其他渲染器。

Substance Painter 的其他著色器可以在 Substance Share[&#128279;](https://share.allegorithmic.com/libraries?by_category_type_id=6) 找到。

>[!NOTE]
>
> 著色器 API 也可直接從應用程式使用，透過「說明>文件」選單 **> Shader API** 即可使用。

## 著色器參考

## 更新日誌

* [完整變更日誌檔案](changelog-shader-api.md)

## 熱身

在 Substance Painter 裡，你可以用 GLSL *自己寫著色器*。我們只允許你撰寫 *片段* 著色器的一部分，有時也稱為 *表面著色器*。 事不宜遲，讓我們介紹「Hello world」Substance Painter 表面著色器：

```
void shade(V2F inputs) { 

  diffuseShadingOutput(vec3(1.0, 0.0, 1.0)); 

}
```


現在，如果你把這段片段存成 *.glsl* 檔案，然後把它丟進 Shelf 的著色器分頁，載入 Substance Painter，你就可以使用它，並在網格上看到漂亮且均勻的粉紅色。

## 表面著色器

* [surface-shader.glsl](shaders-shader-api/surface-shader-shader-api.md)

## 引擎提供的資料（或者我該如何存取我的頻道？）

在 Substance Painter 裡，你可以存取渲染引擎的參數（文件通道、額外材質、相機相關資料等等）。 以下是所有引擎所提供參數的詳細清單：

* [all-engine-params.glsl](parameters-shader-api/all-engine-params-shader-api.md)

## 引擎設定（或我該如何指定渲染狀態？）

在某些情況下，你可能會想使用特定的渲染配置（剔除、混合、取樣區域性等）來達成效果。 部分渲染狀態會被暴露，可以在著色器中設定。 以下是所有暴露渲染狀態的完整清單：

* [All-Rendering-States-Params.GLSL](parameters-shader-api/all-rendering-states-params-shader-api.md)

## 自訂調整（或者我該怎麼調整我的著色器？）

在著色器裡做自訂調整是很常見的。 為了在 Substance Painter 的著色器中做到這一點，我們引入了一種可以指定自訂調整的方式。 以下是所有自訂著色器調整類型的詳細清單：

* [All-Custom-Params.GLSL](parameters-shader-api/all-custom-params-shader-api.md)

## 嵌入式函式庫

為了避免在所有著色器中寫大量模板程式碼，我們建立了一個小而實用的函式庫。 **請注意，目前您無法編輯或自行創建。**

* [lib-alpha.glsl](libraries-shader-api/lib-alpha-shader-api.md) ：包含與不透明度相關的輔助工具
* [lib-bayer.glsl](libraries-shader-api/lib-bayer-shader-api.md) ： 包含拜耳矩陣輔助工具
* [lib-defines.glsl](libraries-shader-api/lib-defines-shader-api.md) ： 包含有用的數學常數
* [lib-emissive.glsl](libraries-shader-api/lib-emissive-shader-api.md) ： 包含 Emissive Properties 輔助工具
* [lib-env.glsl](libraries-shader-api/lib-env-shader-api.md) ：包含環境地圖相關的輔助工具
* [lib-normal.glsl](libraries-shader-api/lib-normal-shader-api.md) ：包含與法線貼圖相關的輔助工具（以及高度圖生成的法線貼圖）
* [lib-pbr.glsl](libraries-shader-api/lib-pbr-shader-api.md) ：包含物理基礎的渲染輔助工具
* [lib-pbr-aniso.glsl](libraries-shader-api/lib-pbr-aniso-shader-api.md) ：包含各向異性物理基礎渲染輔助工具
* [lib-pom.glsl](libraries-shader-api/lib-pom-shader-api.md) ：包含視差遮蔽映射輔助工具
* [lib-random.glsl](libraries-shader-api/lib-random-shader-api.md) ：包含隨機工具（低差異序列）
* [lib-sampler.glsl](libraries-shader-api/lib-sampler-shader-api.md) ：包含通道獲取器輔助工具
* [lib-sparse.glsl](libraries-shader-api/lib-sparse-shader-api.md) ：包含安全的稀疏紋理取樣輔助工具
* [lib-ss.glsl](libraries-shader-api/lib-sss-shader-api.md) ： 包含次表面散射輔助工具
* [lib-utils.glsl](libraries-shader-api/lib-utils-shader-api.md) ：包含色彩工具函式（sRGB 轉換、色調映射）
* [lib-vectors.glsl](libraries-shader-api/lib-vectors-shader-api.md) ： 包含常見向量輔助工具

## 元資料

你可以申報額外的非必要資訊，給渲染系統一些提示。 以下是語法：

```
//: metadata { 

//:   "key1":"value1", 

//:   "key2":"value2" 

//: }
```


支援的金鑰有：

* **custom-ui**：以自訂的 QML 模組取代標準著色器參數的使用者介面（詳見腳本文件）。 路徑可以是絕對路徑，也可以是相對於你 *架子上的自訂介面* 資料夾。
* **mdl**：定義 Iray MDL 材質，讓它搭配著色器使用。 路徑語法如下： *mdl：:folder1::folder2:：mdl\_filename：：material\_name* 其中 *folder1：:folder2:：mdl\_filename* 是你架子 *mdl* 資料夾內通往 mdl 檔案的路徑，而 *：：material\_name* 是該 mdl 檔案中宣告的材質名稱。 （例如：「MDL」：「MDL：:alg::materials::p hysically\_metallic\_roughness：:p hysically\_metallic\_roughness」）

## 範例著色器（是的，終於有了！）

為了體驗看起來像真實著色器的感覺，以下是幾個範例著色器，依複雜度遞增排序：

* [pixelated.glsl](shaders-shader-api/pixelated-shader-api.md) ：一個像素化著色器
* [toon.glsl](shaders-shader-api/toon-shader-api.md) ：一個 Toon 著色器
* [pbr-metal-rough.glsl](shaders-shader-api/pbr-metal-rough-shader-api.md) ：Substance Painter 中嵌入的預設 PBR 著色器

## 動態材質分層

動態材質分層是一種特定的工作流程，將材質在著色器中混合在一起，讓使用者能在 Substance Painter 中動態編輯混合遮罩。 為了實現此工作流程，新增了兩項功能：

* 宣告從著色器定義中可編輯堆疊： [layering\_declare\_stacks.glsl](parameters-shader-api/layering-declare-stacks-shader-api.md)
* 將材質綁定為著色器參數： [layering\_bind\_materials.glsl](parameters-shader-api/layering-bind-materials-shader-api.md)
