---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/pipeline-and-integration/installation-and-preferences/retrieving-the-installation-path.html"
breadcrumb-title: ''
description: 學習如何取得 Substance 3D Painter 的安裝路徑，用於腳本撰寫與管線整合。
helpx_creative_field: ""
helpx_description: Painter > Pipeline and integration > Installation and preferences > Retrieving the installation path
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 取回安裝路徑
user-guide-description: ''
user-guide-title: ''
source-git-commit: 22871eab2f25d09bd82f1292d8b3e5f8c4f1c2cf
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 1%

---


# 取回安裝路徑

本頁彙整了根據版本與平台，如何取得應用程式安裝路徑的資訊。

## 窗戶

### 創意雲端桌面

1. 開啟 Windows 登錄檔編輯器（**regedit**）。
1. 請前往登錄檔鍵：** HKEY\_LOCAL\_MACHINE\Software\Microsoft\Windows\CurrentVersion\App Paths\**
1. 打開名為 **Adobe Substance 3D 的子鍵Painter.exe**
1. 該金鑰的值包含應用程式執行檔安裝地點的路徑

>[!NOTE]
>
> 此登錄檔金鑰僅自 7.2 版本起提供。\
>  對於較舊版本，安裝路徑可從 HKEY\_CURRENT\_USER\Software\Microsoft\Windows\CurrentVersion\ Explorer\FileExt **的檔案關聯**&#x200B;中取得。

### Substance 3D 獨立版

1. 開啟 Windows 登錄檔編輯器（**regedit**）。
1. 導航到登錄檔鍵：**HKEY\_LOCAL\_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall**
1. 找出與你應用程式版本 AppID 相符的子金鑰（見下表）
1. 該密鑰的值包含通往應用程式安裝位置的路徑

| 版本 | AppID |
| --- | --- |
| **版本 1.x** | `{410F5B6E-A29C-4F43-9DE3-44A1357D6AF5}` |
| **版本 2.x** | `{f42b7a996fa1d13a1d0a2e33eea2c0800bb5d1b8}` |
| **3.x（2017.x）至7.1** | `{33C3E9E2-0675-4196-9019-28AB9C5E9BB0}` |
| **7.2 或更新版本** | `{2a8bbb68-725b-477c-9194-60efc5ece348}` |

### 蒸汽

該應用程式安裝在 **Steam 安裝資料夾的 steamapps/common/** 子資料夾中。

## 麥克

在 Mac 上，該應用程式安裝於以下格式：

| 版本 | 路徑 |
| --- | --- |
| **7.2 或更新版本** | **/應用程式/Adobe Substance 3D Painter.app** |
| **遺產** | **/應用/物質 Painter.app** |

## Linux

在 Linux 上，rpm 套件的安裝路徑如下：

| 版本 | 路徑 |
| --- | --- |
| **7.2 或更新版本** | **/opt/Adobe/Adobe\_Substance\_3D\_Painter** |
| **遺產** | **/opt/寓言/實質\_Painter** |
