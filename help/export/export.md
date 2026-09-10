---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/getting-started/export.html"
breadcrumb-title: ''
description: 學習如何從 Substance 3D Painter 匯出各種格式的材質，供其他應用程式和遊戲引擎使用。
helpx_creative_field: ""
helpx_description: Painter > Getting Started > Export
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 匯出
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---


# 匯出

## 匯出材質

貼圖會匯出成一組點陣圖。 Painter 在匯出貼圖時因為有 Output 模板，提供了很大的彈性。 輸出範本讓你可以控制匯出檔案的命名、貼圖如何打包到通道裡，以及匯出檔案的格式和位元深度。 如果這聽起來有點嚇人，別擔心，Painter 包含數十個預設輸出範本，針對常用的 3D 應用和使用情境設定。

你可以打開 <b>匯出視窗</b> ，開始用 <b>檔案>匯出貼圖</b>，或使用鍵盤快捷鍵 <b>CTRL + SHIFT + E</b>。請使用以下連結了解更多關於匯出貼圖的資訊：

* [匯出視窗](../export/export-window/export-window.md)
* [輸出範本](../export/export-presets/export-presets.md)
* [修改或建立輸出範本](creating-export-presets.md)

### 匯出你的網格

例如，Painter 可以自動產生 UV，修改你匯入的網格。 如果你在 Painter 裡對網格做了修改，可以用檔案 > 匯出網格</b>匯出<b>。

匯出網格時，你會有幾個選項：

* <b>無位移/拼貼：</b>匯出基礎網格，且不根據材質修改幾何體。
  * <b>套用三角剖</b>分：如果匯入的網格是由四邊形或多邊形組成，你可以啟用這個選項來匯出 Painter 三角化版本的網格。 這有助於避免其他應用程式在三角定位方式不同時出現視覺三角定位的錯誤。
* <b>使用位移/鑲嵌</b>：Painter 會對網格進行拼貼，增加更多多邊形，並利用位移或高度來改變網格的表面幾何形狀。
  * <b>重新計算頂點法線</b>：修改網格表面可能導致先前頂點的法線不正確。 啟用此選項後，Painter 會自動將頂點法線更新為新曲面的正確值。

![](../assets/export-render.jpg){width="500px"}
