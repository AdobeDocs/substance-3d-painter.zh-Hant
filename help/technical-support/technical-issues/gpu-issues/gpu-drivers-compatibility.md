---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/technical-issues/gpu-issues/gpu-drivers-compatibility.html"
breadcrumb-title: ''
description: 了解 Substance 3D Painter 對 GPU 驅動程式的相容性要求，以確保渲染穩定與效能。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > GPU Issues > GPU drivers compatibility
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: GPU 驅動程式相容性
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---


# GPU 驅動程式相容性

本頁彙整了有關可能導致 Substance 3D Painter 問題的 GPU 驅動程式資訊。

## Nvidia

下表列出所有已知會對 Nvidia GPU（GeForce 或 Quadro 型號）造成問題的驅動版本：

| *驅動版本* | *問題描述* |
| --- | --- |
| <b> 425.xx </b> | GPU 光線追蹤的瑕疵。 |
| <b> 429.xx 或更早版本 </b> | 黑色材質方塊的瑕疵。 |
| <b> 435.xx 或更舊版本 </b> | sRGB 色彩在計算貼圖時的問題。 |
| <b> 439.xx </b> | 材質損毀。 |
| <b> 441.08 </b> | 當機或穩定性問題。 |
| <b> 442.19 </b> | 當機或穩定性問題。 |
| <b>528.09</b> | 作業系統當機。 |
| <b>572.16 到 572.42</b> | 烘焙貼圖時會出現瑕疵或當機。 |

### AMD

| *驅動版本* | *問題描述* |
| --- | --- |
| **20.7.x**  至  **20.11.2** | 材質出現故障或損壞。 |
| **20.11.3**  至  **21.2.1** | 材質出現故障或損壞，還有當機或穩定性問題。 |
| **21.2.3**  至 **21.6.1** | 當機或穩定性問題。 |
