---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/technical-support/technical-issues/stability-issues/crash-while-baking.html"
breadcrumb-title: ''
description: 學習如何修復 Substance 3D Painter 在烘焙操作中當機的問題，以實現可靠的貼圖烘焙工作流程。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Stability Issues > Crash while baking
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 烘焙時撞擊
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---


# 烘焙時撞擊

Substance 3D Painter 在某些設定的烘焙過程中可能會當機。 本頁彙整了已知問題及其緩解方法。

## 烘焙崩潰預覽

預設情況下，Substance 3D Painter 會在視窗中顯示材質烘焙的進行狀態。 在某些電腦上，這個特性可能會導致不穩定。

要停用它：

1. 使用  **編輯>設定**  開啟主要設定
1. 在一般模式下&#x200B;**往下滑到名為**「烘焙選項&#x200B;**」的區**&#x200B;塊。
1. 取消勾選/停用啟用即時預覽烘焙流程&#x200B;**的選項**。

## GPU 光線追蹤當機

在某些驅動程式不穩定的 GPU 上，烘焙過程可能會因為 GPU 光線追蹤功能而當機。

要停用它：

1. 使用  **編輯>設定**  開啟主要設定
1. 在一般模式下&#x200B;**往下滑到名為**「烘焙選項&#x200B;**」的區**&#x200B;塊。
1. 取消勾選/停用啟用 GPU 光線追蹤&#x200B;**的選項**。

## Ryzen CPU 當機

該應用程式在某些使用 Ryzen CPU 的電腦設定中，可能會在烘焙過程中當機。 通常更新 BIOS 就能解決問題。

這與多執行緒計算有關。 許多主機板製造商已發布新的 BIOS 更新以修正此問題，因此我們建議您進行更新。 更多資訊請參閱主機板手冊及製造商網站。

## 不相容的 Assbin 檔案

預設烘焙時，高多邊形網格會預先處理成  **\*.assbin**  檔案，以便後續加速重新烘焙。 在某些罕見情況下，若這些檔案是用不同版本產生的，可能會導致應用程式當機。 只要刪除它們，問題就會解決，因為它們會被重新生成。
