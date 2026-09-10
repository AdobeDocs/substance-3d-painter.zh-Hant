---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/technical-support/technical-issues/stability-issues/crash-during-export.html"
breadcrumb-title: ''
description: 學習如何修復 Substance 3D Painter 在匯出作業中當機，以實現可靠的貼圖匯出工作流程。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Stability Issues > Crash during export
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 出口時崩潰
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---


# 出口時崩潰

某些特定情況會導致 Substance 3D Painter 在匯出時當機，尤其是在非常高解析度（例如 4K 或 8K）時。 以下是此問題最常見的來源清單。

## TDR（超時偵測與恢復）

逾時偵測與恢復（TDR）是 Microsoft Windows 的一種安全機制，用來防止 GPU 在無止盡的計算中鎖死系統。 這個機制對 Substance 3D Painter 來說預設限制過多。

更多資訊請參見：[GPU 驅動程式因長時間計算而當機（TDR 當機）。](https://helpx.adobe.com/tw/substance-3d/unlisted/documentation/spdoc/gpu-drivers-crash-with-long-computations-128745489.html)

## 低虛擬記憶體

匯出可能會消耗大量記憶體（電腦記憶體），當系統用盡記憶體時，系統會嘗試回退虛擬記憶體。 虛擬記憶體通常是儲存在硬碟上的額外記憶體。 如果虛擬記憶體容量太小，Substance 3D Painter 會當機，因為記憶體用盡了。

更多資訊請參見： [低虛擬記憶體](crash-with-low-virtual-memory.md)當機。

## 磁碟空間不足

自從 Sparse Virtual Textures（SVT）推出後，Substance 3D Painter 可以在磁碟上串流出一些快取以平衡效能。 如果硬碟空間不足，可能會導致當機，因為應用程式無法傳輸和寫入快取。

快取位置可以從預設的系統暫存檔案資料夾中移動。 更多資訊請參見： [稀疏虛擬貼圖](../../../features/sparse-virtual-textures.md)。

## 超頻的 GPU 頻率

超頻的 GPU 通常會比較不穩定，因為它們運行的頻率並非最初由 GPU 建構者設計。 暫時關閉超頻可能會有幫助。

更多資訊請參見： [超頻 GPU](../gpu-issues/crash-when-working-with-overclocked-gpu.md) 當機。
