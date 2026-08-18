---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/painting/dynamic-strokes/creating-custom-dynamic-strokes.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中創造自訂動態筆觸，以設計獨特的筆觸行為與效果。
helpx_creative_field: ""
helpx_description: Painter > Painting > Dynamic strokes > Creating Custom Dynamic Strokes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 建立自訂動態筆劃
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---


# 建立自訂動態筆劃

為了建立自訂動態筆劃，有兩種選項可供選擇：

* 利用現有的 Substance 資源來建立新的畫筆/工具預設
* 從零開始建立新的 Substance 資源（需要 [Substance 3D Designer）。](https://substance3d.adobe.com/display/SDDOC/Substance+Designer)

同時建議在建立自訂 Substance 檔案前，先閱讀 [Dynamic Stroke Performances](dynamic-stroke-performances.md) ，以避免任何問題。

## 重複利用現有資源

從零開始創建新的動態筆劃可能很困難。 利用現有資源、微調，然後儲存成新的預設，這已經是個不錯的起點。

在 Shelf 上找到適合你需求的資源，然後看看我們的預設[](../presets/presets.md)頁面。

## 為動態筆劃建立自訂 Substance 檔案

以下是 Substance 圖中動態筆劃所支援的參數列表。

| 變數識別碼 | 說明 |
| --- | --- |
| <b>隨機種子</b> | 如果 Substance 檔案在 Random Seed 曝光時製作，則可透過動態筆觸功能控制。 |
| <b>郵票索引</b> | <b>Integer1</b> 在上色筆觸時會由 Substance 3D Painter 提供。 最小值和最大值不會影響，Substance 3D Painter 會忽略它們。 |
| <b>stampCycleCount 郵票週期計數</b> | <b>Integer1</b> Painter 會讀取參數的預設值、最小值和最大值，以揭露印章循環計數參數。 這個參數控制會創造出多少獨特的物質變體。 |
| <b>$time</b> | <b>Float1</b> 在繪製筆觸時，會根據每筆的經過時間（每筆）由 Substance 3D Painter 餵食。 這種特性會產生許多物質變化，進而影響表現。 |
| <b>行程間距</b> | <b>float1</b> 為整個筆劃的當前間距值。 |
| <b>筆劃大小</b> | <b>float1</b> 為整筆繪製的當前大小值。 |
| <b>印章筆劃位置</b> | <b>integer1</b> 用於指定筆劃的開始與開始。 最終值只能在路徑筆劃上取得，無法透過手動繪畫取得。 可能的價值：<ul data-preserve-html="true"> <li data-preserve-html="true">0 = 中間</li> <li data-preserve-html="true">1 = 開始</li> <li data-preserve-html="true">2 = 結束</li> </ul>可使用 isstrokepositionactive 用戶標籤停用。 |
| <b>距離沿曲線</b> | <b>float1</b> 在給定印記沿路徑上的當前距離。 這種特性會產生許多物質變化，進而影響表現。 可以用 <b>iscurvedistanceactive</b> 用戶標籤來停用。 |
| <b>距離MaxCurve</b> | <b>float1</b> 指使用 path 工具所建立路徑的總長度。 可以用 <b>iscurvedistanceactive</b> 用戶標籤來停用。 |
| <b>pathCorner</b> | <b>整數1</b> 表示色帶所使用的角型。 可能的價值：<ul data-preserve-html="true"> <li data-preserve-html="true">0 = 無角</li> <li data-preserve-html="true">1 = 左角</li> <li data-preserve-html="true">2 = 右角</li> </ul> |
| <b>pathCornerAngle</b> | <b>將角角在帶狀路徑上的弧度浮點</b> 。 可用來根據精確角度值補償或調整角落的外觀。 |
| <b>patchLengthOnCurve</b> | <b>浮動</b> Size 為 Ribbon 路徑上的一個區段（patch）。結合 <b>distanceAlongCurve</b> 和 <b>distanceMaxCurve</b> ，可以用來正規化一個區域的大小。 |
