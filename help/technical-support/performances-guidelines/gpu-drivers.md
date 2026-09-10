---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/technical-support/performances-guidelines/gpu-drivers.html"
breadcrumb-title: ''
description: 了解 Substance 3D Painter 對 GPU VRAM 和驅動程式的需求，以優化渲染效能與穩定性。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Performances guidelines > GPU Drivers
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: GPU 顯存與驅動程式
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 0%

---


# GPU 驅動程式

沒有使用推薦驅動程式，我們無法保證效能。 非 WHQL 駕駛者必須避免。\
GPU 驅動程式就像任何軟體一樣，每次新版本都可能帶來效能問題。 若在更新到較新驅動版本後出現問題，我們建議將驅動程式降級到先前版本。

## NVIDIA 驅動程式設定

有些 NVIDIA 預設設定會影響效能，我們建議建立設定檔並關閉以下參數（設定為關閉）：

* 執行緒優化
* 垂直同步

## 其他應用程式如何利用 GPU

Substance 3D Painter 並非唯一使用 GPU 的軟體，其他應用程式也同樣如此。 幾乎所有 3D 應用程式都會使用 GPU 和 VRAM 來執行，包括常見於 Painter 的軟體，如 Blender、Maya、Unreal Engine、Unity、C4D 等。 確保良好效能同時保持這些應用程式開放的解決方案，是確保 Substance 3D Painter 先啟動，然後申請自己的 VRAM 分配。 不過，有些軟體可以動態取得 VRAM 的部分功能，即使它們是在 Painter 之後推出，仍可能與 Substance 3D Painter 發生衝突。

一般來說，Painter 能存取的 VRAM 越多，執行速度就越快，因此盡量減少其他應用程式同時與 Painter 同時運行的 VRAM 使用量。

## GPU VRAM 的容量與頻寬

Substance 3D Painter 大部分運算都依賴 GPU。 這就是為什麼擁有符合 [系統需求的](../../getting-started/system-requirements.md) GPU 非常重要。

Painter 的運作方式是將貼圖轉移到 GPU 記憶體（VRAM）中，以便進行計算（例如混合操作以產生最終貼圖）。 不過，如果 VRAM 開始滿，未使用的材質會被傳回電腦的 RAM，以釋放 VRAM 空間。 Substance 3D Painter 在工作時會寫入和讀取數 GB 的資料。 這表示 VRAM 的容量（容量）和傳輸時的頻寬速度都很重要。 你可以使用像 [MSI AfterBurner](https://www.msi.com/page/afterburner) 這類工具來監控這種行為。

>[!NOTE]
>
> <b>Nvidia GTX 970</b> 以其 GPU 記憶體設計有問題而聞名，這影響了 Substance 3D Painter。整個 4GB 裡最後 500MB 的速度比剩下的 3.5GB 慢。 如果 Substance 3D Painter 能在最後 500MB 上運作，效能可能會降低多達 10 倍（根據我們測量的）。 欲了解更多技術細節，請參見： <https://www.pcper.com/news/Graphics-Cards/NVIDIA-Responds-GTX-970-35GB-Memory-Issue>
