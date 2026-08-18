---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/painting/advanced-channel-painting/normal-map-painting.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中直接繪製法線貼圖，為材質增添表面細節和深度。
helpx_creative_field: ""
helpx_description: Painter > Painting > Advanced channel painting > Normal Map Painting
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 法線貼圖繪製
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 0%

---


# 法線貼圖繪製

繪製細節可以透過直接在網格上繪製法線貼圖資料來完成。 本頁將整理不同的法線貼圖繪製方式。

## 繪製法線貼圖細節

要繪製法線貼圖細節：

1. 在目前的材質集（如果還沒有）中新增一個普通通道
1. 在目前繪畫工具中啟用法線通道
1. 在目前繪畫工具的材質區塊的普通欄位載入一個普通資源。

從那裡開始，使用法線貼圖繪製與高度貼圖繪製[&#128279;](height-map-painting.md)非常相似，但多了烘焙法線的精準度。

![](../../assets/normal-painting.gif)

## 一般混合模式

法線貼圖在圖層堆疊中有自己的混合模式：

* **法線貼圖細節**  （預設）
* **法線貼圖反細節**
* **法線貼圖結合**

想了解它們，請參閱 [混合模式](../../interface/layer-stack/blending-modes.md) 頁面。

## 正常色彩空間

當將法線貼圖載入材質的槽位（工具屬性或填充層）時，可以更改預設色彩空間。

此設定可用來指定法線貼圖格式，因為預設情況下預期會有 DirectX（Y-）法線貼圖（不受專案設定影響）。 因此，使用 OpenGL （Y+） 法線貼圖時，必須點擊小箭頭開啟色彩空間選單，然後更改點陣圖的色彩空間。

![](../../assets/normal-color-space.png)

## 在烘焙的法線貼圖上繪製

在某些情況下，能夠覆蓋烘焙的法線貼圖以隱藏細節（甚至修正烘焙問題）會很有用。\
Substance 3D Painter 的專案預設設定不允許這樣做，因為它會分別計算法線通道和烘焙法線。 此行為可透過 [貼圖集設定](../../interface/texture-set/texture-set-settings.md) 來更改。

### 1 - 更改材質集混合模式

預設情況下，會建立一個貼圖集，並將&#x200B;**一般混音**&#x200B;設定設為合併&#x200B;**&#x200B;**。

為了覆蓋或繪製法線貼圖，重要的是將此設定設為  **替換**  。 法線貼圖會從視窗中消失，這是預期中的。 將此模式改為  **替換**  表示 Substance 3D Painter 在產生最終法線貼圖時，只考慮法線通道和高度通道。

![](../../assets/normal-mixing.png)

### 2 - 用烘焙的法線貼圖設定填充層

建立新的填充層，然後透過屬性面板將烘焙的法線放入「法線」槽中。 如果填充層的預設耕耘值沒設為 1，別忘了更改。

![](../../assets/fill-layer_1.gif)

### 3 - 更改填充層混合模式

預設情況下，任何新圖層法線通道的混合模式都設為「法線貼圖細節」。 因為最好用填充層作為基礎，我們選擇了「正常」混合模式，因為點陣圖沒有 alpha，會取代下面的所有部分（包括著色器的預設顏色）。

![](../../assets/blending-mode.gif)

### 4 - 建立一個圖層來覆蓋烘焙的法線貼圖

建立一個新圖層（普通或填充），並將其混合模式改為「正常」，適用於正常通道。 設定完成後，任何繪在法線通道上的元素都會接管底層的烘焙法線貼圖。

![](../../assets/normal-painting-over.gif)
