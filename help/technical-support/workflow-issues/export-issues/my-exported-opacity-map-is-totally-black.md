---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/technical-support/workflow-issues/export-issues/my-exported-opacity-map-is-totally-black.html"
breadcrumb-title: ''
description: 學習如何修正匯出的不透明度貼圖在 Substance 3D Painter 中完全呈現黑色，以便正確匯出透明。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Workflow Issues > Export Issues > My exported opacity map is totally black
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 我匯出的不透明度貼圖完全是黑色的
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---


# 我匯出的不透明度貼圖完全是黑色的

當你建立新專案時，預設顏色來自著色器，而不是貼圖。 因此，當你匯出所有沒上色的零件時，它們會變成黑色，alpha 值設為 0（因為這些零件沒有資料）。

最簡單的解決方法是在圖層堆疊底部放置一個填充圖層：它會用預設顏色填滿所有 UV，該顏色與著色器的預設顏色相同。
