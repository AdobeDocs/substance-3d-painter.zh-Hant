---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/technical-issues/gpu-issues/multi-bi-gpu.html"
breadcrumb-title: ''
description: 學習如何為多GPU及雙GPU系統配置Substance 3D Painter，以優化渲染效能。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > GPU Issues > MultiBi-GPU
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 多雙顯卡
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# 多 GPU 與雙 GPU

部分 GPU 配置和/或 GPU 型號與 Substance 3D Painter 不相容，會導致不穩定與當機。 以下是不相容配置的列表：

| ***配置*** | ***解法*** |
| --- | --- |
| **Nvidia SLI / AMD Crossfire**    （顯示卡橋接器） | 在顯示卡驅動設定中關閉 SLI 或 Crossfire。 |
| **雙顯示卡**    （兩組GPU晶片組裝在一張顯示卡上） | 在驅動程式設定中關閉兩顆 GPU 晶片組，只用其中一顆。 |
