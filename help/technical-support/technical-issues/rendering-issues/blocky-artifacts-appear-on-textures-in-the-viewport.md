---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/technical-issues/rendering-issues/blocky-artifacts-appear-on-textures-in-the-viewport.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 視口中修正貼圖上出現的方塊狀瑕疵，以提升乾淨的視覺品質。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Rendering Issues > Blocky artifacts appear on textures in the viewport
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 方塊狀的瑕疵會出現在視窗的材質上
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---


# 方塊狀的瑕疵會出現在視窗的材質上

從 2018.3.0 版本開始，視窗中會出現以下類型的雜訊：

![](../../../assets/viewport-artifacts.jpg){width="400px"}

這些瑕疵與 Nvidia GPU 驅動程式的問題有關。\
為避免這些瑕疵，稀疏虛擬材質硬體支援需要停用。

**GeForce 驅動程式 440.97** 現在&#x200B;**已經修正了這個問題**。我們建議更新這些驅動程式，並保持啟用 SVT 以獲得良好效能。

Nvidia 官網已提供新驅動程式： <https://www.nvidia.com/Download/index.aspx>

## 停用稀疏虛擬貼圖硬體加速

### 1 - 啟動 Substance 3D Painter 並開啟設定

![](../../../assets/settings-34.png)

透過編輯>設定開啟主要設定。

### 2 - 尋找名為「稀疏虛擬貼圖」的區塊

![](../../../assets/svt-subsection.png)

在「一般」區塊中，往下滑找到名為「稀疏虛擬貼圖」的子區塊。

### 3 - 取消勾選設定

![](../../../assets/uncheck-hardware.png)

取消勾選「硬體支援加速」設定。

### 4 - 驗證並重新啟動 Substance 3D Painter

![](../../../assets/validate-1.png)

點擊「確定」按鈕驗證變更。

![](../../../assets/restart-3.png)

點擊「是」按鈕重新啟動 Substance 3D Painter 以套用變更。
