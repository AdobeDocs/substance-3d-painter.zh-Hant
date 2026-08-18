---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/features/post-processing/color-profile.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中使用色彩輪廓後製來套用色彩調色和 LUT 轉換。
helpx_creative_field: ""
helpx_description: Painter > Features > Post Processing > Color Profile
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 色彩特徵
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 0%

---


# 色彩特徵

![](../../assets/doc-lut-example.jpg){width="700px"}

Substance 3D Painter 允許透過載入 **LUT** 材質，將色彩設定&#x200B;**檔指派**&#x200B;到&#x200B;**視窗**。\
色彩配置可以用來校準螢幕的最終顏色，以匹配目標，例如特定攝影機。 設定檔通常會透過改變亮度、伽瑪、對比度甚至色彩平衡來操控顏色。

>[!NOTE]
>
> **LUT** 代表「**Look Up Table」（查找表**）。 這是作為後期效果進行色彩分級的優化方式。 LUT 用來彌補來源與結果之間的差異。\
>  Substance 3D Painter 使用 **3D** LUT 以 2D 貼圖&#x200B;**（浮動）形式儲存**，解析度不限（預設為 **2048x128 像素**）。這表示儲存色彩操作的立方體會分成並排顯示的切片。 更多技術細節，請參閱  **GPU Gem**  文章： <http://http.developer.nvidia.com/GPUGems2/gpugems2_chapter24.html>

## 使用色彩配置

色彩設定檔可透過顯示設定視窗載入。\
勾選「  **啟用色彩設定檔**  」的勾選框，影響視窗並啟用色彩設定檔。

![](../../assets/color-profile-ui.png)

* 當「啟用色彩輪廓」被  **停用**  時，材質視圖的視窗渲染會以  **sRGB**  進行（某些特定通道則是線性）
* 當啟用&#x200B;**&#x200B;**「啟用色彩設定檔」時，視口的渲染會以&#x200B;**線性/原始格式（Linear/RAW**）呈現所有視角（包括單頻道）。

如果在資源槽載入了 LUT 貼圖，則在材質  **模式下**  會用來操作視口的渲染。\
否則渲染會顯示為線性/RAW（例如單頻道視圖）。

**白點**&#x200B;設定可用來改變輸入影像的色調映射（在 LUT 生效前）。\
例如，如果你看的是太陽，這個值應該要高於1（預設值）。 為了達到完美曝光，白點必須設定為影像的高明值。

白點公式如下：

```
float Value = 1.0f / WhitePoint; // Value from the user interface 

float3 Output = clamp( HDR.rgb * Value, 0.0f, 1.0f );
```


在使用色彩設定檔前，可以先套用特定的色調映射。 請參閱音調映射[&#128279;](tone-mapping.md)中的函式。\
Substance 3D Painter 除了透過白點設定外，不會處理輸入顏色。 例如，沒有套用 Shaper LUT。

## 建立色彩設定檔

當啟用「**啟用色彩配置檔」時，Substance 3D Painter 會將**&#x200B;視口切換成&#x200B;**線性**&#x200B;渲染。這表示當 LUT 被應用時，需要將線性剖面的顏色轉換到目標。

### 方法一：修改身份LUT

編輯身份 LUT 可以在支援 <b>32 位元浮動</b> 紋理的軟體中完成，例如 <b>Substance 3D Designer</b>。 下載身份 LUT 作為建立新設定檔的起點：

[下載 color\_profile\_linear.exr](https://github.com/AdobeDocs/painter-python-api/raw/refs/heads/main/static/misc/color_profile_linear.exr)

### 方法二：使用 OpenColor IO 產生 LUT 材質

安裝  **OpenColor 的 IO**  工具。 接著下載範例 OCIO 配置，請點此取得： <http://opencolorio.org/downloads.html>\
接著，執行  **ociolutimage**  程式，並使用以下參數：

```
ociolutimage --generate --cubesize 64 --config nuke-default/config.ocio --colorconvert linear srgb --output lutLinearToSRGB.exr
```


**注意**：也可以透過 ocioconvert **程式對 Identity LUT 進行色彩轉換，並透過 OpenColor IO** **修改 Identity LUT**。

### 匯入新的色彩設定檔

只要打開匯入視窗（或拖放 LUT 到書架上即可）。 在 Substance 3D Painter 匯入 LUT 材質時，務必將「  **colorlut**  」  **的使用**  分配到新的資源上。 否則資源在架子上就看不清楚。

欲了解更多資訊，請參閱關於匯入新資源的文件： [透過匯入視窗新增資源](https://helpx.adobe.com/tw/substance-3d/unlisted/documentation/spdoc/adding-content-via-the-import-window-151584824.html)
