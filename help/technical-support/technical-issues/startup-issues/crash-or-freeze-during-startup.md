---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/technical-issues/startup-issues/crash-or-freeze-during-startup.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 啟動時修復當機與凍結，以穩定啟動應用程式。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Startup Issues > Crash or freeze during startup
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 開機時當機或當機
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 0%

---


# 開機時當機或當機

本頁列出已知問題及其解決方法，與應用程式無法正常啟動相關。

## 軟體衝突

請參考以下頁面，列出所有已知可能造成衝突的軟體： [軟體衝突](software-conflicts.md)。

## 顯示卡不對

如果應用程式無法在正確的顯示卡上啟動，可能會導致穩定性問題。 更多資訊請見此頁面： [Painter 並非從正確的 GPU](../gpu-issues/painter-doesn-t-start-on-the-right-gpu.md) 啟動。

## 過時的 GPU 驅動程式

使用舊的 GPU 驅動程式可能會導致當機和/或當機。 我們建議在有最新顯示卡驅動程式時使用。 看： [GPU 的驅動程式](../gpu-issues/gpu-has-outdated-drivers.md)過時了。

## 螢幕白且無反應

如果應用程式在 Windows 開機時就當機（導致白屏），可能有幾個原因：

* 外部應用程式正在產生衝突，請參見 [軟體衝突](software-conflicts.md) 以了解是哪種衝突。
* 應用程式的部分視窗是在另一台螢幕上開啟的。 將介面恢復為預設配置後，應用程式可正常啟動：
  1. 打開登錄檔編輯器（**從開始選單 regedit** ）
  1. 前往應用程式偏好設定（參見： [偏好設定與應用程式資料位置](https://helpx.adobe.com/substance-3d/unlisted/documentation/spdoc/application-preferences-location-147095594.html)）
  1. 展開 **Adobe Substance 3D Painter** 鍵
  1. 選擇 **Main 視窗 2018** 鍵並刪除它
  1. 重新啟動應用程式

## 因為系統路徑/Python 路徑錯誤而當機

應用程式會檢查系統路徑以載入 Python 模組與環境設定。 如果系統設定錯誤，啟動時可能會當機。

在 Windows 上：

1. 開啟  **開始**  選單
1. 搜尋並選擇系統（  **控制面板）**
1. 點選進  **階系統設定**
1. 點擊  **環境變數**
1. 在系統變數&#x200B;**中**&#x200B;尋找 **PATH** 變數

接著你可以編輯變數來驗證其內容。 例如，如果變數包含這類後續字元，會導致當機

```
ï–›éŒ à €è¸€ì‡ì‡ç¿¹
```


## Windows 10 更新

Windows 10 的某些更新有時會造成不穩定。 使用 Windows 附帶的診斷工具來偵測系統中可能出現的任何錯誤。

我們建議執行  **部署映像服務與管理**  （DISM）及  **系統檔案檢查器**  （SFC）工具。 DISM 有助於恢復 SFC 需要的替換檔案，以修復損壞或遺失的系統檔案。

運行  **DISM**  ：

1. 開啟開始選單
1. 搜尋命令提示字元
1. 右鍵點擊結果，選擇「以管理員身份執行」
1. 輸入以下指令：  **DISM /Online /Cleanup-Image /RestoreHealth**
1. 按下 Enter 鍵

執行  **SFC**  ：

1. 開啟開始選單
1. 搜尋命令提示字元
1. 右鍵點擊結果，選擇「以管理員身份執行」
1. 輸入以下指令：  **sfc /scannow**
1. 按下 Enter 鍵

在執行這兩個指令後重新啟動電腦以套用更新。

欲了解更多相關資訊，請參見：  [使用系統檔案檢查工具修復遺失或損壞的系統檔案](https://support.microsoft.com/en-us/help/929833/use-the-system-file-checker-tool-to-repair-missing-or-corrupted-system)。

## 舊版本啟動時會當機

在 Windows 上，2018 版（4.x）或更舊版本可能無法啟動，因為安裝資料夾附帶的 dll 檔案對作業系統來說過舊。 這個當機可以透過手動替換成較新版本來修復。

要做到：

1. 請前往 Substance Painter 安裝資料夾。
1. 在備份\_libeay32.dll中重新命名libeay32.dll<b><b></b>。</b>
1. 下載以下檔案： [更新\_libeay32.zip](https://helpx.adobe.com/content/dam/help/en/substance-3d/documentation/spdoc/files/182266673/225968681/1/1644000679697/updated-libeay32.zip)。
1. 將 dll 檔案從壓縮檔解壓到安裝資料夾（靠近 Substance Painter.exe 檔案）。
1. 開始申請。
