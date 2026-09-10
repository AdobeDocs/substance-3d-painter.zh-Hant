---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/technical-support/technical-issues/gpu-issues/running-on-integrated-gpu.html"
breadcrumb-title: ''
description: 學習如何將 Substance 3D Painter 設定為專用 GPU 而非整合顯示卡，以提升效能。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > GPU Issues > Running on integrated GPU
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 運行於整合式 GPU 上
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---


# 運行於整合式 GPU 上

![](../../../assets/integrated-gpu.png){width="500px"}

有些電腦預設是用整合晶片組而非專用顯示卡。\
由於整合晶片組的效能非常低，我們建議改用專用 GPU。 彈出式罐子彈出並警告你。

使用 NVIDIA GPU 時，切換到 NVIDIA GPU 取決於應用程式配置檔。 如果應用程式沒有這樣的設定檔，你可以手動分配顯示卡：

1. 右鍵點擊桌面，選擇 NVIDIA 控制面板，  **或**  進入控制面板搜尋 NVIDIA 控制面板
1. 在 3D 設定&#x200B;**中**，請前往&#x200B;**管理 3D 設定**
1. 在程式設定&#x200B;**標籤**&#x200B;下新增 Substance 3D Painter 的設定檔&#x200B;**&#x200B;**
1. 將首選顯示卡設定改為高效能 NVIDIA 處理器
