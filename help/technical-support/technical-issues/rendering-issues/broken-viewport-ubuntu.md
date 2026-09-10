---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/technical-issues/rendering-issues/broken-viewport-ubuntu.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中修復 Ubuntu 上損壞或無反應的視口問題，以實現正確的 3D 渲染。
helpx_creative_field: ""
helpx_description: Viewport appears broken or unresponsive on Ubuntu
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 在 Ubuntu 上，視窗似乎壞掉或無反應
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---


# 在 Ubuntu 上，視窗似乎壞掉或無反應

從 Ubuntu 版本開始，從 Steam 執行 Painter 時，視窗可能會顯示壞掉或無反應。

這是因為 Painter 沒有在正確分配顯示卡時啟動。 在 Ubuntu 上，可能會選擇整合式 GPU 而非獨立顯卡。 Painter 是透過 Steam 繼承這個設定，這可能會造成問題。

有幾種解決方案：

1. 從終端機運行 Steam。 這樣會強制不同的情境，應該能讓 Steam 和 Painter 在正確的 GPU 上運行。
1. 編輯 Steam 捷徑，停用 <b>專用顯示卡</b> 設定的 Run。 然後照常跑 Steam。

更多資訊請參閱 [這個 GitHub 議題](https://github.com/ValveSoftware/steam-for-linux/issues/9940)。
