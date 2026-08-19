---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/technical-support/technical-issues/miscellaneous-issues/error-with-missing-api-ms-crt-dll.html"
breadcrumb-title: ''
description: 學習如何修正 Substance 3D Painter 中缺少的 api-ms-crt DLL 錯誤，以正確支援 Windows 執行時函式庫。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Miscellaneous Issues > Error with missing api-ms-crt dll
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 缺少 api-ms-crt dll 的錯誤
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# 缺少 api-ms-crt dll 的錯誤

Substance 3D Painter 無法啟動，因為  **你的電腦缺少api-ms-win-crt-runtime-l1-1-0.dll**  。\
這很可能是因為 Visual C++ Redistributable **for Visual Studio 2015 的更新KB2999226**&#x200B;未能安裝。

## 要怎麼解決這個問題？

### 1 - 確認 Windows 是否是最新版本

1. 開啟開始選單
1. 選擇控制面板
1. 點擊  **Windows 更新**
1. 點擊「  **檢查」以獲取最新消息**
1. **安裝**  所有可用的更新。
1. 安裝完更新後，請  **重新啟動**  電腦。

重新啟動後重複上述步驟，直到沒有更多更新可用。

### 2 - 安裝 Visual C++ Redistributable

1. 下載 Visual C++ 再發行檔：
   1. 適用於  [Windows 64 位元](http://download.microsoft.com/download/9/3/F/93FCF1E7-E6A4-478B-96E7-D4B285925B00/vc_redist.x64.exe)
   1. 適用於  [Windows 32 位元](http://download.microsoft.com/download/9/3/F/93FCF1E7-E6A4-478B-96E7-D4B285925B00/vc_redist.x86.exe)
1. 執行  **vcredist\_x64.exe**  （64 位元）或  **vcredist\_x86.exe**  （32 位元）
1. 選擇卸載並依照程序操作
1. 再執行一次
1. 選擇安裝
