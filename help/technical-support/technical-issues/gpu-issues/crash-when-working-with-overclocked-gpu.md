---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/technical-support/technical-issues/gpu-issues/crash-when-working-with-overclocked-gpu.html"
breadcrumb-title: ''
description: 了解如何修復 Substance 3D Painter 在使用超頻 GPU 時當機，以維持穩定的應用程式效能。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > GPU Issues > Crash when working with overclocked GPU
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 在超頻顯示卡上工作時會當機
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---


# 在超頻顯示卡上工作時會當機

超頻的 GPU 通常會比較不穩定，因為它們運行的頻率並非最初由 GPU 建構者設計。 如果你的 GPU 超頻且有穩定性問題，我們建議暫時回到出廠預設頻率。

## Nvidia GPU

在 Nvidia GPU 上，從驅動程式 355.82 開始，可以透過在驅動設定中啟用除錯模式，暫時關閉 GPU 超頻。 這讓使用者能夠檢查並判斷與顯示卡相關的問題。

要啟用除錯模式：

1. 打開 **Nvidia 控制面板** （在桌面上右鍵點擊）。
1. 點選說明&#x200B;**&#x200B;**&#x200B;選單。
1. 點擊 **除錯模式**。

>[!NOTE]
>
> 如果你的 GPU 是參考卡，除錯模式可能無法使用。 只有當 GPU 採用非標準時脈或經過修改過的 BIOS 時才會開放。 在這種情況下，我們建議手動關閉超頻功能。
