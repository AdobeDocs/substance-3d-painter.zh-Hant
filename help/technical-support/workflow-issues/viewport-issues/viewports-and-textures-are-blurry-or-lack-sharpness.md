---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/technical-support/workflow-issues/viewport-issues/viewports-and-textures-are-blurry-or-lack-sharpness.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中修正模糊的視窗與材質，以確保畫面銳利清晰。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Workflow Issues > Viewport Issues > Viewports and textures are blurry or lack sharpness
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 視窗和材質模糊或缺乏銳利度
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# 視窗和材質模糊或缺乏銳利度

視窗可能因不同原因而模糊。

## 高 DPI 螢幕（Retina）設定

Substance 3D Painter 預設會將 High-DPI/Retina 螢幕的視窗解析度降細以提升效能。

這種行為可以在主要設定[&#128279;](https://helpx.adobe.com/tw/substance-3d/unlisted/documentation/spdoc/general-71008262.html)中透過更改&#x200B;**視窗縮放**&#x200B;參數來改變。

## 紋理過濾

視窗使用 mipmap 和材質過濾，能夠串流進出 [稀疏虛擬材質](../../../features/sparse-virtual-textures.md) ，以提升效能。 這在某些情況下會導致紋理模糊。

貼圖過濾可以透過顯示設定視窗 [中的視窗視窗中的視窗視窗，在視窗設定](../../../interface/display-settings/viewport-settings.md) 參數下調整。
