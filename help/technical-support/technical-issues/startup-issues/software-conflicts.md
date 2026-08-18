---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/technical-support/technical-issues/startup-issues/software-conflicts.html"
breadcrumb-title: ''
description: 學習如何解決阻礙 Substance 3D Painter 在系統上正常啟動的軟體衝突。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Startup Issues > Software conflicts
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 軟體衝突
user-guide-description: ''
user-guide-title: ''
source-git-commit: 22871eab2f25d09bd82f1292d8b3e5f8c4f1c2cf
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---


# 軟體衝突

本頁列出其他已知可能導致 Substance 3D Painter 當機或無法正常運行的軟體問題。

| *潛在衝突來源* | *子嗣* |
| --- | --- |
| **防毒軟體 / 反間諜軟體** | 防毒軟體或防間諜軟體可能會造成以下一些問題：<ul data-preserve-html="true"> <li data-preserve-html="true"><b> 誤判</b>：Painter 被錯誤標記為病毒或惡意軟體。</li> <li data-preserve-html="true"><b> 被阻擋的檔案</b>：Painter 無法讀取或寫入檔案（匯出、預設建立等）。</li> <li data-preserve-html="true"><b> 檔案刪除</b>：Painter 無法正常啟動或運作，因為必要的檔案已被移除。</li> </ul>若發生上述情況，建議暫時停用防毒軟體看看是否有幫助，或手動為 Painter 新增例外。 |
| **AMD CrossFire 與 NVIDIA SLI** | Painter 不支援多種 GPU 配置，導致當機。 我們建議關閉此功能。 |
| <b> Autodesk 助理</b> | Autodesk 助理應用程式可能會造成衝突，導致應用程式在啟動時或開啟專案檔案時當機。 更新 Autodesk 應用程式以解決問題。 |
| <b> Alienware / Dell 電腦</b> | 更多資訊請參見此頁面： [開啟或儲存檔案](../stability-issues/crash-when-opening-or-saving-a-file.md)時當機。 |
| **Paragon Software 的 APFS** | 此軟體可能會在 Windows 路徑環境變數中註冊一個位置，該位置可能在啟動時導致應用程式當機。 僅僅卸載軟體可能不夠，環境變數可能需要手動移除。 問題地點範例：  `C:Program Files (x86)Paragon SoftwareAPFS for Windowsï–›éŒ à €è¸€ì‡ì‡ç¿¹` |
| **Avecto** | 舊版 Avecto 會造成卡頓和當機。 務必更新到最新版本。 |
| **華碩 GPU 調整** | 此軟體在 Substance 3D Painter 編譯著色器時可能會造成問題，甚至無法啟動著色器編譯。 如果遇到這個問題，我們建議先卸載軟體看看是否能解決問題。 |
| **華碩 RAMCache** | 此軟體可能會阻礙 Substance 3D Painter 正常啟動，或在運行時使其不穩定。 如果你遇到穩定性問題，建議你停用或安裝華碩 RAMCache。 |
| **華碩音速套件** | 在搭載 ASUS 主機板的電腦上，<b>預設可安裝 Asus Sonic Suite</b> 。 卸載此軟體可以修復 Substance 3D Painter 中的一些顯示或介面問題。 |
| **雲端備份軟體**&#x200B;**（** OneDrive、**GDrive、**&#x200B;**Dropbox、**&#x200B;**Filestream 等）** | 雲端備份軟體在儲存專案時，可能會造成多次當機。 如果發生這種情況，建議先處理並儲存專案檔案到非同步資料夾，等不再需要更改時再把專案檔案複製回雲端硬碟。 |
| **奇圖博克斯** | 此軟體在開啟檔案對話框（如開啟或儲存專案）時可能會產生衝突並導致應用程式當機。 你可以在 Chitubox 偏好設定中停用「啟用桌面模型</b>縮圖預覽」這個設定<b>，以避免這個問題。 |
| **二重奏展示** | <b>Duet Display</b> 已知會造成 GPU 驅動程式問題，進而影響 Substance 3D Painter 的行為。 建議你先卸載它。 |
| **Google Chrome** | Google Chrome 在與 Substance 3D Painter 同時運行時，可能會造成一些當機。 為了提升 Substance 3D Painter 的穩定性，建議你更新 Google Chrome 和 GPU 驅動程式。 如果還是會當機，請在 Google Chrome 中關閉硬體加速（這樣 Chrome 就無法使用顯示卡）。 |
| **Nahimic 音訊軟體** | <b>Nahimic</b> 可以凍結或撞擊畫家。 停止它會有幫助，更新也能避免問題。 Nahimic 也執行背景服務，可能會干擾應用程式，可能需要停止或停用。 |
| **Openshot 影片軟體** | <b>Openshot Video Software</b> 可能會與 Substance 3D Painter 在書架預覽中產生衝突。更新 OpenShot 應該能解決問題。 |
| **Pyinstaller** | 此應用程式可能會產生錯誤的環境設定，導致啟動時出錯。 更多資訊請參見 [因 Qt](application-failed-to-start-because-of-qt.md) 而申請未啟動。 |
| **回覆/Plays.tv** | <b>Rptr</b> （或 <b>[Plays.tv]（http://plays.tv/） </b>）預設會搭配部分 GPU 驅動程式安裝。 此軟體可能造成不穩定並導致應用程式當機。 建議卸載該應用程式。 |
| **RGBFusion** | 此軟體可能會與繪圖板驅動程式產生衝突，停止處理程序可暫時解決問題，或移除 RGBFusion 以獲得永久修復。 |
