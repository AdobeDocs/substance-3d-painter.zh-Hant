---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/technical-support/technical-issues/gpu-issues/forcing-the-external-gpu-on-mac-os.html"
breadcrumb-title: ''
description: 學習如何強制 Substance 3D Painter 在 macOS 上使用外接 GPU，以提升渲染效能。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > GPU Issues > Forcing the external GPU on Mac OS
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 在 Mac OS 強制安裝外接 GPU
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---


# 在 Mac OS 強制安裝外接 GPU

在 Mac OS Mojave 上，可以指定每個應用程式使用外接 GPU。 啟用此設定後，Substance 3D Painter 的效能與穩定性可能會提升。

更多資訊請參閱 [蘋果文件](https://support.apple.com/en-us/HT208544)。

啟用它：

1. 如果 Substance 3D Painter 已經在運行，請關閉它。
1. 在 Finder 中選擇 Substance 3D Painter，可以在 Applications **資料夾中找到**&#x200B;**。
1. 按下 **Command-I** 或右鍵點擊 **Substance 3D Painter** 應用程式，選擇 **「取得資訊**」。
1. 在新視窗中，啟用「偏好外接顯示卡&#x200B;**」這個設定**。
1. 重新啟動 Substance 3D Painter。

>[!NOTE]
>
> 如果沒有連接 eGPU，或是目前版本的 MacOS 太舊，這個設定就不會顯示。
