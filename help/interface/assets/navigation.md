---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/interface/assets/navigation.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中操作資產面板，以有效率地瀏覽並存取你的資源庫。
helpx_creative_field: ""
helpx_description: Painter > Interface > Assets > Navigation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 導航
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 0%

---


# 導航

資產視窗中有多種導航方式——麵包屑、搜尋欄位和資產類型圖示。 所有導航類型都是相互依存的，因此你可以將這些搜尋組合起來發揮優勢。\
例如，如果你在資產類型圖示中選擇了材質，但你用麵包屑來導航到 Smart Masks 資料夾，資產面板將不會顯示任何結果——如果你想顯示材質，必須回到「所有資料庫」;想瀏覽智慧遮罩，必須回到「所有資料庫」;如果你想瀏覽智慧遮罩，必須回到「所有資料庫」。

## 麵包屑

麵包屑讓你能快速瀏覽圖書館。 點擊箭頭會顯示資產在磁碟上的儲存方式，並可選擇任何顯示的位置。 如果是灰色，代表該資料夾裡沒有所選資產類型，但你仍然可以導航到該位置。

![](../../assets/00-05-breadcrumbs.jpg)

## 搜尋欄位

搜尋欄位可用來篩選包含該類型查詢的資源。 請注意，它不僅會依資源名稱搜尋，還會搜尋資源的位置，以及資源中包含的任何標籤。\
打字搜尋有時也比單純關鍵字更進階。 請參閱 [進階搜尋查詢](advanced-search-queries.md)。

![](../../assets/00-05-searchfield.jpg)

## 資產類型

>[!NOTE]
>
> 點擊時按住 Ctrl **鍵，可以多重選取**&#x200B;資產類型圖示。

預設選擇是材料，但點擊其他資產類型的圖示會顯示其他類型的資源。

![](../../assets/00-05-assettypeicons.jpg)

| 資產類型 | 說明 |
| --- | --- |
| 材質 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/00-05-assettypes-1-1.png"/></div> | 包含匯入為&#x200B;*基礎材質*&#x200B;的 .sbsar 和從填充圖層建立的材質（你可以在這裡[&#128279;](https://helpx.adobe.com/substance-3d/unlisted/documentation/spdoc/creating-and-saving-a-preset-180191514.html)了解更多關於預設建立的資訊）。它們是基本材質，可用於填充圖層，並會套用到整個網格或材質集的表面。 |
| 智慧材料 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/00-05-assettypes-7.png"/></div> | 包含包含多層儲存在資料夾中的複雜材質（Smart Materials 也是你可以自行建立的預設）。像基礎材質一樣，Smart 材質會套用到整個網格/材質集，但也會考慮網格的個別資訊，例如曲率、遮蔽或其他表面細節。 為了獲得這些表面細節並正確使用智慧材料，首先需要烘焙[&#128279;](../../baking/baking.md)網格。 |
| 智慧口罩 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r3-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/00-05-assettypes-2.png"/></div> | 包含使用多層效果和/或產生器的複雜遮罩。 你可以 [自己建立](https://helpx.adobe.com/substance-3d/unlisted/documentation/spdoc/managing-assets-217187091.html) 智慧口罩的預設。和智慧材質類似，智慧遮罩需要從網格中烘焙的資訊才能正常運作。 |
| 濾鏡 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r4-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/00-05-assettypes-3.png"/></div> | 包含匯入為過濾器&#x200B;*的*.sbsar 檔案。濾鏡是效果，會將你已經存在的材質以某種方式轉化。 有些濾鏡只能用黑白資訊，有些只用材質輸入，這表示不是所有濾鏡都能用在遮罩裡。 |
| 畫筆 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r5-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/00-05-assettypes-4.png"/></div> | 包含畫筆、粒子與工具。 這些都是可以在 [Painter 中建立](https://helpx.adobe.com/substance-3d/unlisted/documentation/spdoc/managing-assets-217187091.html) 的預設。**筆刷** 是基本的黑白預設，使用 alpha 鍵。 你可以用畫筆在任何或所有通道或遮罩中作畫。**粒子** 和畫筆有相同的特性，但它們還有一組額外的參數來模擬與網格的物理互動。 它們能產生溢出、滴水、雨水或其他需要物理模擬的現象。**工具** 可以包含刷子和/或粒子行為，但這個預設也會隨材質通道資訊一起儲存。 |
| 阿爾法 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r6-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/00-05-assettypes-5.png"/></div> | 包含多種 alpha 圖，以及數個筆 [刷製作器，可製作](https://helpx.adobe.com/substance-3d/unlisted/documentation/spdoc/managing-assets-217187091.html) 更具複雜效果的畫筆（如類似 Photoshop 的動態筆觸、畫輥）。Alpha 是灰階影像，黑色部分在使用時看起來是透明的。 |
| 材質 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r7-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/00-05-assettypes-6.png"/></div> | 包含垃圾搖滾、程序化、烘焙貼圖、硬表面法線和 LUT。**垃圾** 搖滾是帶有有趣噪音和紋理的灰階影像。 它們可以用來為網格表面增加變化，無論是透過遮罩，或直接插入通道。**程序化動畫** 也是包含噪音甚至規則圖案的灰階材質。 然而，與某些靜態的 grunge 不同，程序生成是動態點陣圖，可以無重複縮放，且透過隨機種子有無限變化。**烘焙貼圖** 代表從網格中擷取的表面與形狀資訊。 想了解更多烘焙相關資訊，請參考這裡。**硬表面法線** 是你可以直接用法線通道印在網格上的細節。**LUT** （查找表）是色彩配置貼圖，可以在顯示設定中模擬視窗中的色彩配置檔行為。 你可以在這裡[&#128279;](../../features/post-processing/color-profile.md)了解更多關於色彩輪廓的資訊。 |
| 環境地圖 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r8-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/00-05-assettypes-1.jpg"/></div> | 包含匯入為 *環境* 的影像（最常見的是 .hdr 或 .exr）。環境貼圖是背景影像，能自動產生光照設定。 你可以直接拖曳環境貼圖到視窗，或是進入顯示設定。 |
