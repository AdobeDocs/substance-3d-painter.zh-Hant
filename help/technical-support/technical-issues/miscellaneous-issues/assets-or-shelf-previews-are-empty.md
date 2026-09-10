---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/technical-support/technical-issues/miscellaneous-issues/assets-or-shelf-previews-are-empty.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中修復空的資產和書架預覽，以恢復縮圖顯示功能。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Miscellaneous Issues > Assets (or shelf) previews are empty
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 資產（或書架）預覽是空白的
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---


# 資產（或書架）預覽是空白的

此問題可能由其他軟體引起，詳見： [軟體衝突](../startup-issues/software-conflicts.md)。

如果無法確定是哪個軟體在更新或卸載，請找一個名為「QT\_PLUGIN\_PATH」的環境變數並移除它。

**在 Windows 上：**

1. 控制面板開啟 **系統** 。
1. 在進階分頁，點選 **環境變數**
1. 找名為 **「QT\_PLUGIN\_PATH」的變數。**
1. **把它拿掉**
1. **重新啟動** 你的電腦
