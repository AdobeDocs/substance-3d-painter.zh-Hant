---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/technical-issues/stability-issues/windows-blue-screens.html"
breadcrumb-title: ''
description: 學習如何在使用 Substance 3D Painter 以穩定系統運作時，避免 Windows 藍屏錯誤。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Stability Issues > Windows Blue Screens
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Windows 藍屏
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---


# Windows 藍屏

在 Windows  [上，藍屏死機（BSOD）](https://en.wikipedia.org/wiki/Blue_screen_of_death)  通常與驅動程式或硬體故障有關。 Substance 3D Painter 本身不會導致藍屏死機，但因為應用程式非常密集，它能稍微釐清電腦本身的問題。 以 Substance 3D Painter 為例，藍屏死機可能由以下問題引起。

## GPU 驅動程式不穩定

Substance 3D Painter 很大程度上依賴 GPU 來執行各種運算。 GPU 驅動程式有時會不穩定或出現退化現象。 我們建議保持 GPU 更新，以獲得最新的修正與效能提升。 看： [GPU 的驅動程式](../gpu-issues/gpu-has-outdated-drivers.md)過時了。

### 不穩定的 Windows 安裝

Windows 本身在更新後可能會不穩定。 使用 Windows 附帶的診斷工具來偵測系統中可能出現的任何錯誤。

我們建議執行  **部署映像服務與管理**  （DISM）及  **系統檔案檢查器**  （SFC）工具。 DISM 有助於恢復 SFC 需要的替換檔案，以修復損壞或遺失的系統檔案。

運行  **DISM**  ：

1. 開啟  **開始選單**
1. 搜尋  **命令提示字元**
1. **右鍵點擊**  結果，選擇「  **以管理員**  身份執行」
1. 輸入以下指令：  **DISM /Online /Cleanup-Image /RestoreHealth**
1. 按下  **Enter 鍵**

執行  **SFC**  ：

1. 開啟  **開始選單**
1. 搜尋  **命令提示字元**
1. **右鍵點擊**  結果，選擇「  **以管理員**  身份執行」
1. 輸入以下指令：  **sfc /scannow**
1. 按下  **Enter 鍵**

在執行這兩個指令後重新啟動電腦以套用更新。

欲了解更多相關資訊，請參見：  [使用系統檔案檢查工具修復遺失或損壞的系統檔案](https://support.microsoft.com/en-us/help/929833/use-the-system-file-checker-tool-to-repair-missing-or-corrupted-system)

### 磁碟空間不足

自從 Substance 3D Painter 引入 [稀疏虛擬貼圖](../../../features/sparse-virtual-textures.md) 後，應用程式現在在工作時會利用磁碟快取貼圖。 如果系統空間不足，就可能導致不穩定。

這個問題有兩個簡單的解決方案：

* 釋放一些磁碟空間，讓快取系統有更多空間。
* 把快取目錄移到空間較大的硬碟上。 這個位置可以透過進入應用程式的主要設定來更改，詳見  [「暫存檔案」設定](https://docs.substance3d.com/display/SPDOC/General)  。

### 硬碟故障（硬碟或固態硬碟）

如前所述，快取系統非常依賴磁碟。 如果磁碟機故障，系統在嘗試寫入或讀取資料時可能會不穩定。

要偵測磁碟是否有故障，可以在 Windows 上執行 CHKDSK：

1. 打開  **星號選單**
1. 選擇  **電腦 / 此電腦**
1. **在你的硬碟上右鍵點擊**  ，選擇  **「屬性」。**
1. 切換到  **工具**  標籤。
1. 在錯誤檢查&#x200B;**下**&#x200B;點選「**檢查/立即**&#x200B;檢查」。

### 記憶體故障

記憶體（RAM）故障可能導致系統不穩定，若程式無法安全地讀寫記憶體。 為了檢查記憶體完整性，我們建議執行  **MemTest**。

請參考  [這份安裝與使用 MemTest 的指南](https://www.memtest86.com/technical.htm)  。
