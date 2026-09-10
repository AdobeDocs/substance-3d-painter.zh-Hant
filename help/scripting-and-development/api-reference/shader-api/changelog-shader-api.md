---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/scripting-and-development/api-reference/shader-api/changelog-shader-api.html"
breadcrumb-title: ''
description: 請參閱 Substance 3D Painter Shader API 的更新日誌，以追蹤更新、新功能與變更隨時間的變化。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API > Changelog - Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Changelog - Shader API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 3%

---


# Changelog - Shader API

## 更新日誌

## 2018.3.2

* [lib-sparse.glsl](libraries-shader-api/lib-sparse-shader-api.md)：取樣函式使用貼圖導數，而非簡單的 mipmap 層級。 這是支持各向異性取樣的必要條件。 抽樣函數的簽名不會被修改。
* [lib-pom.glsl](libraries-shader-api/lib-pom-shader-api.md)： *getParallaxOffset* 函式簽名已更改，以使用紋理導數

## 2018.3.0

* 新增一個 [lib-pbr-aniso.glsl](libraries-shader-api/lib-pbr-aniso-shader-api.md) 函式庫，幫助視覺化各向異性鏡面高光
* 新增一個 [lib-sparse.glsl](libraries-shader-api/lib-sparse-shader-api.md) 函式庫，以協助通道取樣，同時照顧 mipmaps 的可用性
* 更新著色器函式庫介面以維護這些安全取樣
* **棄用**：先前基於 vec2 紋理座標與紋理取樣器的函式已被棄用（請使用新簽章）
* [lib-pom.glsl](libraries-shader-api/lib-pom-shader-api.md)：新增一個 *applyParallaxOffset* 函式，簡化視差遮蔽效果的使用
* [lib-random.glsl](libraries-shader-api/lib-random-shader-api.md)：新增藍噪聲隨機值產生器及時間替代方案
* [lib-sampler.glsl](libraries-shader-api/lib-sampler-shader-api.md)：將所有通道取樣輔助拆分，同時擁有值解讀與取樣輔助

## 2018.2.0

* **Surface 著色器 API 變更**： *著色* 函式簽名已更改，詳見 [surface-shader.glsl](shaders-shader-api/surface-shader-shader-api.md)
* *shadeShadow* 函式已不再使用，且可安全從自訂表面著色器中移除
* 新增次表面散射支援，詳情請參見 [surface-shader.glsl](shaders-shader-api/surface-shader-shader-api.md) 和 [lib-sss.glsl](libraries-shader-api/lib-sss-shader-api.md)
* [lib-pbr.glsl](libraries-shader-api/lib-pbr-shader-api.md)： *pbrComputeBRDF* 函式已被移除。 請參考 [pbr-metal-rough.glsl](shaders-shader-api/pbr-metal-rough-shader-api.md) 範例，了解如何使用該函式庫
* 新增了引擎參數： *材質_blue_noise*、 *畫面_ratio*、 *鏡頭_vp_matrix_inverse*、 *環境_exposure*、 *環境_rotation*、 *視野*、 *主鏡頭_light* 畫面 *_size*。 詳情請參見 [all-engine-params.glsl](parameters-shader-api/all-engine-params-shader-api.md)
* 新增 *描述* 元資料，提供自訂著色器參數的工具提示

## 2017.4.2

* 修正文件範例中缺少的著色器（像素化和卡通著色器）
* 修正抖動以達到高解析度
  * [lib-bayer.glsl](libraries-shader-api/lib-bayer-shader-api.md)： **bayerMatrix8（）** 回傳座標 > 4k 的有效值

## 2017.4.1

* 修正 pbr 塗層著色器
  * [lib-vectors.glsl](libraries-shader-api/lib-vectors-shader-api.md)： **tangentSpaceToWorldSpace（）** 和 **worldSpaceToTangentSpace（）** 的輸出現在已經正規化

## 2017.4.0

* 某些網格在 2D 視角中出現錯誤的鏡面反射

## 2017.3.1

* 較便宜的抖動

## 2017.2.0

* 移除插值的 TBN 正規化，以符合 Substance Designer 和 Baker 的行為
* [視窗]將哈默斯利表換成斐波那契螺旋

## 2.6.0

* 修正著色器混合與剔除模式
* 重新設計抖動。 如果渲染是線性渲染，我們會在色彩配置後套用

## 2.5.0

* 新增對視窗色彩設定檔（LUT）的支援（可選 sRGB 轉換）
* 在著色器中加入抖動不透明度
* 在 PBR 著色器中加入視差遮蔽貼圖
* 新增一個方法，可以從預設著色器介面中隱藏自訂參數
* 新增圖層著色器文件中通道標籤列表的連結
* 將「channel\_ao」標籤替換為「channel\_ambientocclusion」
* [視窗]有些法線貼圖有壓縮值，會呈現出雜訊
* 在著色器文件中修正可用通道
* 允許定義自訂著色器使用者介面
* 新增一個標準的自訂著色器介面來做材質分層著色器
* 自訂 UI 檔案現在會相對地在書架上的 shaders/custom-UI 資料夾搜尋（類似 mdl）。
* 在預設著色器中使用鏡面關卡通道
* 修正 vec3 著色器參數範例
* 升級 Painter 至 OpenGL 核心設定檔

## 2.4.0

* 修正匯出法線貼圖和視窗顯示法線貼圖的差異

## 2.2.0

* 在非文件材質中新增無綁定材質的支援
* 更新自訂著色器滑桿文件
* 允許定義滑桿的步進精度
* 動態材質分層的文件

## 2.1.1

* 在 lib-utils 中新增一個「RGB2Gray」函式

## 2.1.0

* 允許定義著色器參數和材質/遮罩的群組
* 在文件中新增缺少的通道（如「ao」、「diffuse」、「specularlevel」）。

## 2.0.4

* 正常解包函式在低 alpha 值下錯誤
* 允許在自訂著色器中讀取網格頂點顏色
* [視窗]部分電腦上的拉伸環境地圖

## 2.0.0

* 允許依專用頻道覆蓋 Normal/AO 額外地圖
* 將 Height2Normal 函式改為使用 Sobel 方法
* 新增每個著色器定義 mdl 的可能性
* 在書架上新增一個 mdl 資料夾
* 新增漫射與鏡面級聲道預設
* 音調映射的文件更新
* 在正字法模式下固定反射
* 修正了環境圖中特定位置出現的垂直白色故障
* 允許定義貼圖參數的「default\_color」

## 1.7.0

* 允許取樣外部材質（從書架）

## 1.6.0

* Exping gamma/tonemapping 功能，讓它們可以覆寫
* 暴露多個texcoords

## 1.5.0

* 在著色器錯誤報告中新增行號和檔名

## 1.4.1

* 所有 sRGB 轉換都遵循 sRGB 標準，除了在著色器中進行的近似轉換
* 高度通道轉為法線貼圖時，被轉換成錯誤的色彩空間

## 1.4.0

* 新增環境遮蔽通道
* 新增一般版工作流程
* 為貼圖相關的自動參數新增「或」表達式語法
* 修正 OSX 上 Intel 顯卡的 PBR 著色器問題

## 1.3.4

* 允許在片段著色器中插值雙法性
* 修正 Mikkt 切空間

## 1.3.3

* 固定產生負光強度的球諧波
* 曝光計算與 Substance Designer（以及固定曝光滑桿）不同
* 陰影不應該在100%金屬表面上可見

## 1.3.0

* 新增陰影函數
* 新增不透明度支援（&#39;alpha\_test&#39; 和 &#39;alpha\_blend&#39;）

## 1.2.0

* 能夠將所需的 openGL 狀態設定成自訂著色器
* 修正倒切二字
* 新增對一般頻道的支援

## 1.0

* 新增自訂著色器的支援
