---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/technical-support/technical-issues/rendering-issues/mesh-appears-pink-in-the-viewport.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 視角中修正粉紅色網格外觀，以恢復正確的材質渲染。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Rendering Issues > Mesh appears pink in the viewport
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 網格在視窗中呈現粉紅色
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---


# 網格在視窗中呈現粉紅色

![](../../../assets/pink-mesh.jpg){width="400px"}

網格在視窗內會呈現&#x200B;**粉紅色**，因為&#x200B;**繪製的**&#x200B;著色器&#x200B;**不再編譯**（如日誌視窗&#x200B;**所述**）。這可能是因為過時的著色器不支援最新版本的著色器 API。

以下是解決方法：

* 對於&#x200B;**預設著色器**：請依照「更新著色器[&#128279;](../../../interface/shader-settings/updating-a-shader.md)」頁面的逐步步驟操作。
* 關於 **自訂著色器**：請查看日誌視窗中的錯誤訊息以及 [著色器 API](https://helpx.adobe.com/tw/substance-3d/unlisted/documentation/spdoc/custom-shader-api-89686018.html) 頁面。
