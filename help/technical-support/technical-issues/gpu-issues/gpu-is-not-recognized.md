---
breadcrumb-title: ""
description: 學習如何在 Substance 3D Painter 中修復 GPU 識別問題，以啟用正確的硬體加速與效能。
title: GPU 未被識別
user-guide-description: ""
user-guide-title: ""
source-git-commit: 6b6d52207ca1d043aaa1b2b14145b6b49d4c1942
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%
---

# GPU 未被識別

![](../../../assets/not-recognized-gpu.png){width="500px"}

有些  **NVIDIA Optimus**  用戶可能會遇到讓 Substance 3D Painter 在正確顯示卡上運行的問題。 一個變通方法是將 Windows 登錄檔中的以下金鑰設為 0：

* HKEY\_LOCAL\_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Windows\RequireSignedAppInit
* HKEY\_LOCAL\_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Windows NT\CurrentVersion\Windows\RequireSignedAppInit
