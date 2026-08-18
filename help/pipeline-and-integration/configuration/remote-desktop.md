---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/pipeline-and-integration/configuration/remote-desktop.html"
breadcrumb-title: ''
description: 學習如何設定 Substance 3D Painter 以實現遠端桌面存取，以實現遠端工作流程與協作。
helpx_creative_field: ""
helpx_description: Painter > Pipeline and integration > Configuration > Remote Desktop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 遠端桌面
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---


# 遠端桌面

本頁說明了讓 Substance 3D Painter 能在 Windows 上透過遠端桌面（RDP）執行的解決方案與替代方案。

預設情況下，Windows 上的 RDP 運行在不存在或過低的 OpenGL 環境中，導致應用程式無法正常運作或當機。 Substance 3D Painter 需要 OpenGL 3.3 上下文。 以下是緩解問題的解決方案，但無法保證它們一定有效，因為最初的問題依賴於 Windows 和部分 GPU 驅動程式。

>[!NOTE]
>
> Nvidia Quadro GPU 預設可以 RDP 模式執行應用程式，而 Nvidia GeForce GPU 僅提供 OpenGL 1.4 上下文（對 Substance 3D Painter 來說太低）。 可以安裝執行檔來解決這個問題，詳見： <https://developer.nvidia.com/designworks>

## Windows 政策設定

在 Windows 10 上，可能需要更改  **群組原則**  ，才能讓 GPU 在 RDP 模式下執行。

要做到：

1. 按  **Win + R**  開啟執行視窗
1. 輸入「  **gpedit.msc**  」然後輸入
1. 導覽至  **本地電腦政策\電腦設定\管理範本\Windows 元件\遠端桌面服務\遠端桌面會話主機/遠端會話環境**
1. 啟用「使用硬體預設顯示卡」的選項  **，適用於所有遠端桌面服務會話**  。

## Windows TSCON 指令

如果之前的政策變更沒用，你可以試著用  **tscon**  指令列。 這個指令會斷開遠端電腦，並將一台新的電腦連接到實體硬體（滑鼠、鍵盤等）。 接著只要遠端執行應用程式並重新連線，應該就能在 GPU 上操作該應用程式。

1. 按下  **Windows+R**  鍵即可開啟  **執行**  視窗。
1. 輸入  **cmd**  並按  **Enter**  。
1. 在命令列類型及以下指令中：  **tscon 1 /dest:console**
1. 按下 Enter 鍵
1. 在命令列輸入下一個指令：  **開始「Path/To/Substance/Painter/Folder/Substance 3D Painter.exe」（**  記得更改路徑以符合你的電腦）
1. 按下 Enter 鍵

完成這些步驟後，等幾秒讓應用程式啟動，然後再重新連接你的工作階段。

如果這個步驟無法運作，你可能需要在管理員模式下執行 Windows 命令列。

## 替代方案

如果之前的建議還是不行，我們建議使用像是VNC或Teamviewer這類支援遠端連線GPU的替代方案。
