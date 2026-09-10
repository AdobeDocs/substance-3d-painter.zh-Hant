---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/interface/display-settings/environment-settings.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中設定環境設定，以控制光線和背景以進行材質預覽。
helpx_creative_field: ""
helpx_description: Painter > Interface > Display settings > Environment settings
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 環境設定
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---


# 環境設定

顯示設定&#x200B;**的**&#x200B;這個區塊控制視窗中的光照。

## 環境

![](../../assets/env-settings.png)

| *背景設定* | *描述* |
| --- | --- |
| **環境地圖** | 環境貼圖貼圖用來照明場景。 可以在資產[&#128279;](../assets/assets.md)視窗中使用「環境」預設找到。點擊按鈕即可開啟迷你書架並選擇不同的環境地圖。 |
| **覆蓋環境地圖色彩空間** | 如果目前專案使用 [Color management](../../features/color-management/color-management.md)，可以啟用此設定來覆蓋環境貼圖的色彩空間。 |
| **環境不透明度** | 控制視窗背景中環境貼圖的可見性與透明度。 這些設定對場景的光線沒有影響。 |
| **環境暴露** | 曝光值（EV）是一個代表固定場景亮度的數字。 此設定允許偏移預設亮度值。當使用應用程式提供的環境貼圖時，此設定應維持在 0。 若素材曝光值不正確，可能會在其他應用中產生色彩校正問題。 |
| **環境旋轉** | 控制環境貼圖的水平旋轉。 這對於旋轉場景中的光線和改變物件的反應很有用。 可以用捷徑[&#128279;](../settings/shortcuts.md)控制。 |
| **環境模糊** | 控制環境材質在視窗背景中呈現的銳利或模糊程度。 這些設定對光線沒有影響。 |
| **環境對齊** | 控制環境貼圖如何在視窗內圍繞 3D 模式旋轉。 此設定可用於在局部設定時點亮 3D 模型下方的區域。可能的數值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>世界</strong> （預設）：環境與場景對齊，並繞著 3D 模型的上軸旋轉。</li><li data-preserve-html="true"><strong>局部</strong>：環境與相機對齊，並繞攝影機的上軸旋轉。</li></ul> |

## 陰影

![](../../assets/shadow-2.png)

| *背景設定* | *描述* |
| --- | --- |
| **陰影** | 啟用/停用視窗中陰影渲染。 |
| **計算模式** | 控制陰影計算的速度。<ul data-preserve-html="true"><li data-preserve-html="true"><strong> 密集 </strong> 度：計算速度快，但可能會凍結視窗的渲染。</li><li data-preserve-html="true"><strong> 平均 </strong> ：密集模式與輕量級模式的平均值。</li><li data-preserve-html="true"><strong> 輕量 </strong> 級 ：（預設）計算會讓陰影在幾秒內變慢，但不會拖慢視口的效能。</li></ul> |
| **陰影的不透明度** | 控制場景中可見的陰影量。 |
