---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/painting/dynamic-strokes/enabling-dynamic-stroke-feature.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 啟用動態筆觸功能，以創造具有可變效果的響應式筆觸。
helpx_creative_field: ""
helpx_description: Painter > Painting > Dynamic strokes > Enabling Dynamic Stroke Feature
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 啟用動態筆劃功能
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 2%

---


# 啟用動態筆劃功能

要啟用動態筆觸功能，首先需要特定資源。

## 尋找 Dynamic Strokes 相容資源

瀏覽資產[&#128279;](../../interface/assets/assets.md)視窗時，縮圖右下角有專用圖示顯示資源的相容性類型。如果沒有顯示圖示，代表該資源無法利用該功能。

| *聖像* | *描述* |
| --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/icon-dyn.png"/></div> | 此資源可採用以下一項或多項行為：<ul data-preserve-html="true"><li data-preserve-html="true">郵票索引</li><li data-preserve-html="true">時間</li><li data-preserve-html="true">隨機種子</li></ul> |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/icon-random.png"/></div> | 這個資源只暴露隨機種子參數。 |

也可以透過書架中的搜尋欄位搭配以下關鍵字搜尋資源：

* 動態行程
* 隨機種子

## 動態筆劃參數

![](../../assets/dynamic-strokes-settings.png)

當 Dynamic Stroke 資源載入後，會在 Substance 參數群組之前新增一個參數清單。

| *參數* | *描述* |
| --- | --- |
| **動態控制** | 列出目前使用的 Substance 檔案可用的參數。 |
| **郵票起始** | 只有當該資源擁有動態控制「印花索引」時才可用。 表示筆觸內印章索引應從哪個數值開始：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>從一開始（0）：</strong>預設。 每筆劃一筆，索引從零開始。</li> <li data-preserve-html="true"><strong>來自隨機索引</strong>：索引從隨機值開始（最大值由印花循環計數定義）。 請注意，以下數值仍為順序，並非完全隨機。</li> </ul> |
| **郵票週期計數** | 只有當該資源擁有動態控制「印花索引」時才可用。 這些參數控制 Substance 3D Painter 何時停止產生新的 Substance 變體，開始回收現有變體。 這個參數對表現有很大影響，你可以閱讀更多關於動態擊球表現[&#128279;](dynamic-stroke-performances.md)的相關資料。 |
| **隨機種子類型** | 只有當資源有動態控制「隨機種子」時才可用。 控制隨機種子的變化方式：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>單人</strong>：預設。 使用一個隨機種子值，可以透過物質參數手動設定。</li> <li data-preserve-html="true"><strong>每筆劃</strong>隨機：每筆刷產生一個新的隨機種子值。</li> <li data-preserve-html="true"><strong>隨機每個印章</strong>：在刷筆內為每個印章產生新的隨機種子值。 <em><strong>要小心參數，因為這可能非常昂貴</strong>。</em></li> </ul> |
| **時間** | 時間動態控制沒有任何參數。 時間是由畫筆劃的長度決定的。 |

## 相容工具列表

動態筆劃設定僅能在以下工具與情境中使用：

| *工具類型* | *相容資源槽* |
| --- | --- |
| **油漆** | <ul data-preserve-html="true"><li data-preserve-html="true">Alpha</li><li data-preserve-html="true">材質</li></ul> |
| **橡皮擦** | <ul data-preserve-html="true"><li data-preserve-html="true">Alpha</li><li data-preserve-html="true">材質</li></ul> |
| **投影** | <ul data-preserve-html="true"><li data-preserve-html="true">Alpha</li></ul> |
| **污漬** | <ul data-preserve-html="true"><li data-preserve-html="true">Alpha</li></ul> |
| **複製人** | <ul data-preserve-html="true"><li data-preserve-html="true">Alpha</li></ul> |

>[!NOTE]
>
> 動態筆觸與  **粒子**  不相容，因此在物理模式下使用任何工具時此功能會被停用。
