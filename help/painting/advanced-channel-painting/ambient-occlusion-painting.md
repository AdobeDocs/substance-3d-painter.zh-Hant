---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/painting/advanced-channel-painting/ambient-occlusion-painting.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中直接繪製環境遮蔽貼圖，為材質增添逼真的陰影與深度。
helpx_creative_field: ""
helpx_description: Painter > Painting > Advanced channel painting > Ambient Occlusion Painting
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 環境遮蔽繪畫
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---


# 環境遮蔽繪畫

環境遮蔽通道允許在物體的環境陰影中繪製細節。 它可以用來新增來自材質的 AO 細節，或在需要時手動修正烘焙錯誤。

>> 

在電腦圖學中，環境遮蔽是一種陰影與渲染技術，用來計算場景中每個點在環境光下的暴露程度。 管子內部通常比外層表面更被遮蔽（因此更暗），越往管內走，光線就越遮蔽（且越暗）。 環境遮蔽可視為針對每個表面點計算的可及性值。\
資料來源： &lt;https://en.wikipedia.org/wiki/Ambient_occlusion>

**此計算結果**&#x200B;儲存在名為「環境遮蔽」映射的位圖中。此映射可直接在應用程式中烘焙，詳見： [烘焙](../../baking/baking.md)。

## 繪製環境遮蔽

要繪製自訂遮蔽細節，需要環境遮蔽通道。 可以透過貼圖集設定](../../interface/texture-set/texture-set-settings.md)新增[：

![](../../assets/add-ao-channel.png)

一旦通道加入貼圖集，任何圖層都可以用來繪製新的資訊。 由於 AO 通道僅包含灰階資訊，建議的混合模式為 **Normal** （繪製覆蓋）和 **Multiply** （合併）。

想了解更多關於它們以及如何依頻道切換，請參見： [混合模式](../../interface/layer-stack/blending-modes.md)。

## 覆蓋環境遮蔽附加地圖

在某些情況下，將烘焙的環境遮蔽覆蓋會很有用，這樣可以隱藏細節，甚至修復烘焙問題。

Substance 3D Painter 專案的預設設定會將環境遮蔽&#x200B;**通道**&#x200B;與額外貼圖&#x200B;**中的環境遮蔽貼圖**&#x200B;合併。這表示預設無法覆蓋烘焙的額外地圖，因為每個地圖（烘焙地圖與通道）的結果會相乘。 不過，這可以透過以下設定來改變：

### 1 - 新增環境遮蔽通道

在目前材質集中加入一個環境遮蔽通道：\
![](../../assets/edit-ao-channel-optimized.gif)

將混音模式設為「  **取代**  」而非「  **乘法**  」：\
![](../../assets/ao-mix-mode.gif)

### 2 - 用烘焙的環境遮蔽設定填充層

建立新的填充層，並將烘焙好的環境遮蔽放入「環境遮蔽」槽中，透過屬性面板。 如果填充層還沒設成 1，別忘了更改預設的耕耘。\
![](../../assets/ao-stack.png)

### 3 - 更改填充層混合模式

預設情況下，AO 通道在任何新圖層的混合模式都設定為「  **乘法**  」。 因為最好用填充層作為基礎，我們選擇了「正常」混合模式，因為點陣圖沒有 alpha，會取代下面的所有部分（包括著色器的預設顏色）。\
![](../../assets/ao-blend-mode.gif)

### 4 - 建立一個圖層，用來覆蓋烘焙的環境遮蔽貼圖

建立一個新圖層（普通或填充），並將 AO 通道的混合模式改為「normal」。 一旦完成這個設定，AO 通道上繪製的任何東西都會接管下面圖層中烘焙好的 AO 貼圖。\
![](../../assets/paint-over-ao-optimized.gif)
