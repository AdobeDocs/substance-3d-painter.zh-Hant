---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/features/post-processing/tone-mapping.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中使用色調映射後製，調整視窗中的曝光與色彩調色。
helpx_creative_field: ""
helpx_description: Painter > Features > Post Processing > Tone Mapping
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 色調對應
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 0%

---


# 色調對應

![](../../assets/tone-mapping.png)

色調映射參數允許控制顏色如何縮放以顯示在螢幕上。 這些設定對於重新分配顏色非常有用，因為它們的數值範圍很廣（甚至可能超過目前螢幕能顯示的範圍）。

>[!NOTE]
>
> Substance 3D Painter 輸出  **HDR**  （高動態範圍）顏色（在線性伽瑪空間），但大多數螢幕只能顯示  **低動態範圍（LDR**  ）顏色。 為了將 HDR 範圍映射到 LDR 範圍，必須進行轉換。 這就是音調映射的原理。

| *背景設定* | *描述* |
| --- | --- |
| **曝光** | 在施加眩光效果或調映射之前，先調整 HDR 空間渲染結果。 |
| **伽瑪** | 這是伽瑪校正的伽瑪值。 |
| **功能** | 用來把 HDR 範圍映射到 LDR 範圍的功能。  可用功能包括：<ul data-preserve-html="true"><li data-preserve-html="true"><strong> 自動 </strong> ：音色映射功能會自動選擇。 預設是 <strong> 感應測量 </strong>  。 </li><li data-preserve-html="true"><strong> 線性 </strong> ：僅此類型輸出顏色未被夾定為0對1。 這對於在應用端實作某些效果時，效果套用後，是最佳選擇。 <br/>除非你有特定理由，否則不建議這麼做，因為如果直接用線性映射作為最終螢幕輸出，高亮度成分會完全消失，高光也會被曝露。</li><li data-preserve-html="true"><strong> LinearSat </strong> ：這幾乎和 <strong> Linear </strong> 一樣，只是輸出顏色是壓縮的。 另外，眩光合成比線性</strong>稍微順<strong>滑一些。</li><li data-preserve-html="true"><strong> 感度測量 </strong> ：在 HDR 空間進行場景渲染時的預設功能。</li><li data-preserve-html="true"><strong>Reinhard </strong> ：這導致映射比感度</strong>測量更為緩慢<strong>，對比度略低。因此，高亮度成分的解析度會提高，並更強地還原明亮部分的亮度變化。</li><li data-preserve-html="true"><strong> ReinhardLum </strong> ：用於實作 <strong> 以亮度為參考並保持原始飽和度（鮮明度：RGB比率）的Reinhard </strong>   色調貼圖類型。 僅將亮度資訊映射到LDR空間，然後重現原始飽和度。 HDR空間的飽和度也會在色調映射後保留。</li><li data-preserve-html="true"><strong>對數</strong>：這導致映射比萊因哈特</strong>更為漸進<strong>，對比度也很低。它使高亮度成分的解析度變得很高，並且在明亮部分能最強烈地還原亮度變化。</li><li data-preserve-html="true"><strong> LogLum </strong> ：用於實作以亮度為參考並保持原始飽和度的對數空間色調映射（鮮明度：RGB比率）。 此方法僅將亮度資訊映射到對數空間，然後重現原始飽和度。 HDR空間的飽和度也會在色調映射後保留。</li></ul> |
| **映射因子** | 這控制了在色調映射過程中映射到最終 LDR 空間的 HDR 空間中亮度（亮度）的最大等級。 超過指定 HDR 空間亮度的顏色無法在 LDR 空間中表示，導致高光過曝。 具體來說，這個值是在HDR空間中（經過曝光縮放後）對應到LDR空間中最大亮度值（1.0）。 在 HDR 渲染模式下，這個數值越低，對比度越高，高光過曝的機率也越高。 相反地，指定較高的數值會降低對比度，降低高光過曝的機率。 在 LDR 渲染模式下，當為了套用效果而重新映射到 HDR 空間時，亮度範圍會擴展至映射因子&#x200B;**中**&#x200B;指定的值。相反地，  **映射因子**  亮度則映射到音調映射時的最大LDR亮度。換句話說，這指定了用於 LDR 渲染結果以應用特效時的動態範圍縮放因子。 將此值設為高值會強調效果中的明亮區域。  **注意：**&#x200B;若函數&#x200B;**在 HDR 渲染模式下**&#x200B;設定為以下任一：線性&#x200B;**、線性衛星**&#x200B;或&#x200B;**&#x200B;**&#x200B;感度測量&#x200B;**，此設定將不影響（**&#x200B;將被忽略）。 |
