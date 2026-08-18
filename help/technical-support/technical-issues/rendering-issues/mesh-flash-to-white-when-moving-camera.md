---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/technical-support/technical-issues/rendering-issues/mesh-flash-to-white-when-moving-camera.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 視口中移動攝影機時，修正網格閃爍成白色的問題，以穩定渲染。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Rendering Issues > Mesh flash to white when moving camera
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 移動攝影機時網格閃光燈轉為白色
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---


# 移動攝影機時網格閃光燈轉為白色

![](../../../assets/white-flash-svt-optim.gif){width="300px"}

舊專案移動時，視窗中的相機可能會短暫出現由白色或空白材質產生的白色閃光。 這是因為  [稀疏虛擬貼圖](https://substance3d.adobe.com/display/DRAFTPAINTER/Sparse+Virtual+Textures)  （SVT）系統依賴特定的著色器配置，而舊著色器並不使用這些設定。

要消除白色閃爍，只需&#x200B;**更新**&#x200B;專案著色器&#x200B;**：**

* 對於&#x200B;**預設著色器**：請依照「更新著色器[&#128279;](../../../interface/shader-settings/updating-a-shader.md)」頁面的逐步步驟操作。
* 自訂 **著色器**&#x200B;方面：請查看日誌中的錯誤訊息以及 [著色器 API](https://helpx.adobe.com/tw/substance-3d/unlisted/documentation/spdoc/custom-shader-api-89686018.html) 頁面。
