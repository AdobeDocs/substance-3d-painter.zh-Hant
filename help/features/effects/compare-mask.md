---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/features/effects/compare-mask.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中使用 Compare Mask 效果，根據貼圖比較操作來建立遮罩。
helpx_creative_field: ""
helpx_description: Painter > Features > Effects > Compare Mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 比較面具
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---


# 比較面具

![](../../assets/compare-mask.png)

此效果能快速且輕鬆地比較兩個通道，並產生遮罩效果。 此效果僅適用於層面罩。

以下是此效果可用的設定：

| 背景設定 | 說明 |
| --- | --- |
| **頻道** | 用來比較來源和目標的通道，以建立遮罩。 這個 LIS 是根據 Texture Set 設定](../../interface/texture-set/texture-set-settings.md)中[可用的通道來決定的。 |
| **比較** | 這裡有三個參數可用來選擇遮罩的計算方式。 中間的下拉選單定義比較運算（小於、在公差範圍內、大於）。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/compare-mode.png"/></div> 來源模式與目標模式分別為：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>下方</strong> 圖層：考慮目前層以下所有圖層的扁平版本。</li><li data-preserve-html="true"><strong>此層</strong> ：僅考慮此層。</li><li data-preserve-html="true"><strong>此遮罩</strong> ：考慮遮罩現有的內容（例如填充效果或生成器效果已存在）。</li><li data-preserve-html="true"><strong>常數</strong> ：均勻值。</li></ul>操作方式如下：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>小於</strong> ：如果來源（左下拉選單）的值低於目標（右下拉選單），遮罩中會輸出白色值。</li><li data-preserve-html="true"><strong>在容差</strong> 範圍內：如果來源（左下拉選單）的值與目標（右下拉選單）相近，遮罩中會輸出白色值。</li><li data-preserve-html="true"><strong>大於：</strong> 如果來源（左下拉選單）的值高於目標（右下拉選單），遮罩中會輸出白色值。</li></ul> |
| **恆定** | 當比較設定設為「常數」時，可以比較的值。 |
| **硬度** | 控制所產生遮罩比較的平滑度與硬度。 |
| **來源通道直方圖** | 提供來源與目標的直方圖視圖。 知道它們是否有重疊或完全沒有重疊很有用（如果沒有重疊，遮罩會是空的）。關於直方圖的更多運作資訊，請參見： [層級](https://experienceleague.adobe.com/en/docs/substance-3d-designer/using/substance-graphs/nodes-reference-for-substance-graphs/atomic-nodes/levels)。 |

>[!NOTE]
>
> 你可以在圖層上右鍵點擊，選擇「**Add mask with height combination**」這個快捷鍵，快速在圖層上新增這個效果。 這個捷徑也會將高度通道 **混合模式** 切換為「**Normal**」，而非預設的「**Linear Dodge （Add）**」。\
> ![](../../assets/compare-shortcut.png)
