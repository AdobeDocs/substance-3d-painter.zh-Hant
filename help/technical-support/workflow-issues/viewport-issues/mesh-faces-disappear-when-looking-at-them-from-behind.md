---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/workflow-issues/viewport-issues/mesh-faces-disappear-when-looking-at-them-from-behind.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 視角中從背後觀看時，解決網格面消失的問題，以便網格能正確看到。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Workflow Issues > Viewport Issues > Mesh faces disappear when looking at them from behind
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 從背後看網狀臉部時會消失
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---


# 從背後看網狀臉部時會消失

預設情況下，視窗中的網格可能不會顯示網格多邊形的背面（背面）。 這是因為它們被目前的著色器剔除。

要顯示臉背面，只需在 [Shader 設定](../../../interface/shader-settings/shader-settings.md)中將當前著色器改為 **pbr-metal-rough-alpha-test**。
