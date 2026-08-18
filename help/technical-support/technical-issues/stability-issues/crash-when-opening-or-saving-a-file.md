---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/technical-issues/stability-issues/crash-when-opening-or-saving-a-file.html"
breadcrumb-title: ''
description: 學習如何修復 Substance 3D Painter 在開啟或儲存檔案時當機，以達成可靠的專案管理。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Stability Issues > Crash when opening or saving a file
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 開啟或儲存檔案時當機
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---


# 開啟或儲存檔案時當機

Substance 3D Painter 在 Windows 開啟檔案對話框時會當機，原因有幾個。 本頁彙整了這個問題的理由與解決方案。

## 軟體衝突

有些程式會新增自訂的 shell 擴充功能，這可能導致不穩定或當機。 可以參考 [軟體衝突](../startup-issues/software-conflicts.md) 清單以獲得更多資訊。

## Shell 擴充功能/自訂主題

我們的 GUI 框架不支援自訂主題，因此強烈建議在使用 Substance 3D Painter 前先卸載目前的主題。

**Alienware**  /  **Dell**  電腦預設整合了一些已知與 Substance 3D Painter 不相容的 shell 擴充。 我們建議你先卸載它們。 雖然我們無法確切知道所有不相容的擴展，但大多數情況下它們對應於：

* DBROverlayIconBackuped.DBROverlayIconBackuped 類別
* DBROverlayIconNotBackuped.DBROverlayIconNotBackuped 類別

您可以使用以下工具查看電腦上安裝了哪些擴充功能。 以下是大致的流程：

1. 從 NirSoft 下載並安裝 ShellExView： <http://www.nirsoft.net/utils/shexview.html>
1. 執行程式
1. 點選  **選項**  並選擇  **依擴充功能類型篩選**
1. 選擇  **圖示覆蓋處理器**
1. 你應該會看到《Alien Respawn **》的兩個條目**。
1. 選擇  **兩個**  ，然後點擊紅色按鈕來停用它們。
