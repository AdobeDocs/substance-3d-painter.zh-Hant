---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/technical-issues/rendering-issues/some-hdpi-scaling-values-are-not-working.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中修正 HDPI 縮放值問題，以獲得適當的高解析度顯示支援。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Rendering Issues > Some HDPI scaling values are not working
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 有些 HDPI 的縮放值無法正常運作
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---


# 有些 HDPI 的縮放值無法正常運作

在 Windows 上，某些 HDPI 縮放值（用於高解析度顯示器介面縮放）可能無法正常運作。\
這是因為我們的視窗框架（Qt）不支援這些。 除非它真正由框架提供者本身管理，否則我們無法修復它。

因此，根據你的設定，你可能會遇到以下行為：

* 120 DPI（**125%** 縮放）- 以 96 DPI（**100%** 縮放）呈現
* 144 DPI（**150%** 縮放）- 呈現為 192 DPI（**200%** 縮放）
* 168 DPI（**175%** 縮放）- 以 192 DPI（**200%** 縮放）呈現

更多詳情請參見： <https://bugreports.qt.io/browse/QTBUG-55654>
