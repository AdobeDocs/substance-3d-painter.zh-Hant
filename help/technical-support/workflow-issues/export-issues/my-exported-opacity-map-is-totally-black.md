---
breadcrumb-title: ""
description: 學習如何修正匯出的不透明度貼圖在 Substance 3D Painter 中完全呈現黑色，以便正確匯出透明。
title: 我匯出的不透明度貼圖完全是黑色的
user-guide-description: ""
user-guide-title: ""
source-git-commit: 6b6d52207ca1d043aaa1b2b14145b6b49d4c1942
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%
---

# 我匯出的不透明度貼圖完全是黑色的

當你建立新專案時，預設顏色來自著色器，而不是貼圖。 因此，當你匯出所有沒上色的零件時，它們會變成黑色，alpha 值設為 0（因為這些零件沒有資料）。

最簡單的解決方法是在圖層堆疊底部放置一個填充圖層：它會用預設顏色填滿所有 UV，該顏色與著色器的預設顏色相同。
