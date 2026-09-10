---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/interface/display-settings/camera-settings.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中設定攝影機設定，以控制視窗攝影機的行為與投影。
helpx_creative_field: ""
helpx_description: Painter > Interface > Display settings > Camera settings
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 相機設定
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 1%

---


# 相機設定

此區&#x200B;**&#x200B;**&#x200B;塊控制相機的行為以及視窗的最終外觀。

## 相機

| *背景設定* | *描述* |
| --- | --- |
| **視野範圍** | 允許控制相機的視角（以度數為單位） |
| **對焦距離** | 定義焦點所在的距離。  這個點被景深效果所利用。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/focus-distance-optim.gif"/></div> **注意：**  對焦距離可以透過快捷鍵 **CTRL + 中鍵點擊網格的某一點來自動設定** |
| **光圈** | 定義景深的寬度。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r3-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/dof-aperture-optim.gif"/></div> **注意：**  如果 Iray 控制此參數，改變它會重新觸發計算。 |

## 後續影響

![](../../assets/post.png)

更多資訊請參閱 [後期效果頁面](../../features/post-processing/post-processing.md) 。

## 時間抗鋸齒

![](../../assets/taa.png)

啟用後， **時間抗鋸齒** （**TAA**）會移除視窗中的鋸齒邊緣。\
**TAA** 透過在多個渲染幀中累積資訊來運作，這表示在攝影機停止移動或執行其他操作之前，該效果會被停用。

| *背景設定* | *描述* |
| --- | --- |
| **累積** | 定義將累積多少幀以減少鋸齒。<ul data-preserve-html="true"> <li data-preserve-html="true">16：大多數情況下的建議價值</li> <li data-preserve-html="true">64：用於清理高對比度值（如 Alpha 測試著色器與抖動結合）</li> </ul>  **注意：**  此設定不影響效能;不過，較高的數值可能會花較長時間才能產生良好結果。 |

![](../../assets/temporal-anti-aliasing.gif){width="500px"}

抗鋸齒也可用於過濾 **Alpha-Test** 著色器，前提是啟用了「**Alpha 抖動**」設定：

![](../../assets/dithering-aa.gif){width="500px"}

## 次表面散射

![](../../assets/subscat.png)

更多資訊請參閱 [次層散射](../../features/subsurface-scattering/subsurface-scattering.md) 頁面。

## 色彩特徵

![](../../assets/profile-13.png)

更多資訊請參閱 [色彩專頁](../../features/post-processing/color-profile.md) 。

## 色調對應

| 背景設定 | 說明 |
| --- | --- |
| **功能** | 指定用於設定超出顯示器顯示能力的色彩值函數（將 HDR 值重新映射至 LDR 範圍）。可能的值有：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>線性</strong> （預設）：無轉換，1.0 以上的數值會被鎖定。</li><li data-preserve-html="true"><strong>ACES：</strong>使用 ACES 的電影色調映射曲線。</li></ul> <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r1-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/linear-vs-aces.jpg" width="450px"/></div> **注意：**  部分遊戲引擎與渲染軟體使用 ACES 色調映射器。 啟用此功能有助於應用程式間匹配顏色，避免差異。 |
