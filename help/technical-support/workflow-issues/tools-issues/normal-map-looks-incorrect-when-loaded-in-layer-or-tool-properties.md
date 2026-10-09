---
breadcrumb-title: ""
description: 學習如何修正 Substance 3D Painter 圖層中的法線貼圖顯示問題，以及工具屬性，以獲得更精確的表面細節。
title: 法線貼圖在圖層或工具屬性中載入時看起來不正確
user-guide-description: ""
user-guide-title: ""
source-git-commit: 6b6d52207ca1d043aaa1b2b14145b6b49d4c1942
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%
---

# 法線貼圖在圖層或工具屬性中載入時看起來不正確

當將法線載入目前工具或填充圖層時，如果是 OpenGL 的法線貼圖，這個法線可能會顯示錯誤。\
原因很簡單：Substance 3D Painter 的引擎預設載入的法線貼圖是 DirectX。

這種行為可以透過點擊物質材料旁的小箭頭或專用頻道輕鬆編輯：

![](../../../assets/channel-format-override.png)
