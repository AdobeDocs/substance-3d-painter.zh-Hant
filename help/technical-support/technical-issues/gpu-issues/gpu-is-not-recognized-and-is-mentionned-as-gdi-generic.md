---
breadcrumb-title: ""
description: 學習如何在 Substance 3D Painter 中以 GDI Generic 識別問題解決，以正確加速 GPU 的效果。
title: GPU 未被識別，並標示為 GDI 通用
user-guide-description: ""
user-guide-title: ""
source-git-commit: 6b6d52207ca1d043aaa1b2b14145b6b49d4c1942
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%
---

# GPU 未被識別，並標示為 GDI 通用

這個問題比較複雜，可能由多種來源造成：

* 如果你使用的是 Nvidia Optimus 的電腦，請參考以下連結： [GPU 無法被識別](gpu-is-not-recognized.md)
* 檢查你的螢幕是否連接到主顯卡（而且在 Windows 上這台螢幕是否被設定為主顯示器）
* 檢查你在 Windows 上主顯示器的色彩位元深度是否設定為 32 位元
* 如果問題還是存在，可以嘗試乾淨重灌顯示卡驅動程式（完全卸載並清除 Windows 登錄檔裡的殘留物）。
