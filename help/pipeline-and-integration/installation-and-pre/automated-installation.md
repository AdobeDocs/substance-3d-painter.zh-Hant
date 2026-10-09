---
breadcrumb-title: ""
description: 學習如何自動化 Substance 3D Painter 安裝，以支援企業部署與管線整合工作流程。
title: 自動化安裝
user-guide-description: ""
user-guide-title: ""
source-git-commit: 6b6d52207ca1d043aaa1b2b14145b6b49d4c1942
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%
---

# 自動化安裝

使用 Substance 3D 獨立安裝程式時，可以將應用程式安裝為靜音模式，方便部署。

我們使用 **InnoSetup** 來產生安裝程式。 安裝程式可用的全部參數都在這裡[&#128279;](http://www.jrsoftware.org/ishelp/index.php?topic=setupcmdline)取得。

## 透過命令列以靜音模式安裝

執行靜默安裝的旗標是 **/SILENT。**&#x200B;**/NCRC** 標誌也可用來跳過套件的 CRC（驗證），以加快流程。

範例：

```
SubstancePainter_Installer.exe /NCRC /SILENT /DIR="C:InstallationFolder"
```


>[!NOTE]
>
> 安裝路徑必須使用單斜線字元來分隔資料夾，否則安裝程式無法辨識該路徑。
