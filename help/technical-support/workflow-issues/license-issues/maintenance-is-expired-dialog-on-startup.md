---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/workflow-issues/license-issues/maintenance-is-expired-dialog-on-startup.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中解決啟動時出現的維護過期對話框，以便管理授權。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Workflow Issues > License Issues > Maintenance is expired dialog on startup
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 啟動時維護是過期對話框
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---


# 啟動時維護是過期對話框

![](../../../assets/expired-mainteance-message.png)

啟動應用程式時，可能會跳出「您目前的維護已過期」的對話框。 本頁列出如何避免此對話的解決方案。

## 解決方案一：更新授權檔案

警告訊息出現是因為授權檔案太舊，需要更新。 只需 **透過應用程式精靈重新啟動產品** 即可。 授權檔案也可透過 Substance 3D 網站手動下載： <https://www.substance3d.com/>。

## 解決方案二：編輯偏好設定來隱藏對話框

>[!NOTE]
>
> 我們建議先嘗試更新授權檔案，再考慮使用這個替代方案。

另一個解決方案是透過設置特定設定來隱藏警告訊息。

導覽至應用程式偏好設定位置：

<table data-preserve-html="true"><colgroup> <col/> <col/> <col/> </colgroup><tbody><tr><th>系統</th><th>版本</th><th>路徑</th></tr><tr><td rowspan="2"><p><strong>窗戶</strong></p><p>（登記處）</p></td><td><strong>7.2</strong> 或更新版本</td><td>HKEY_CURRENT_USER\Software\Adobe\Adobe Substance 3D Painter</td></tr><tr><td>遺產</td><td>HKEY_CURRENT_USER\軟體\寓言\物質畫家</td></tr><tr><td rowspan="2"><p><strong>麥克</strong></p><p>（圖書館）</p></td><td><strong>7.2</strong> 或更新版本</td><td>/使用者/[用戶名]/Library/偏好設定/com.adobe.Adobe Substance 3D Painter.plist</td></tr><tr><td>遺產</td><td>/使用者/[使用者名稱]/Library/Preferences/com.substance3d.Substance Painter.plist</td></tr><tr><td rowspan="2"><strong>Linux</strong></td><td><strong>7.2</strong> 或更新版本</td><td>/home/[username]/.config/Adobe/Adobe Substance 3D Painter.conf</td></tr><tr><td>遺產</td><td>/home/[username]/.config/Allegorithmic/Substance Painter.conf</td></tr></tbody></table>

### 窗戶

要在 Windows 上設定變數，請依照以下步驟操作：

1. 打開開始選單。
1. 搜尋 **Regedit** 即可開啟登錄編輯器。
1. 請前往上表中列出的登錄檔金鑰。
1. 點擊左側樹狀圖中該軟體的登錄檔金鑰。
1. 在右側面板 **的空白區域右鍵點選「新>字串值**」。
1. 新值命名為 **DisableLicenseWarningPopup** ，按 Enter 鍵驗證。
1. 雙擊剛建立的數值。
1. 將 Value data 欄位設為： **true。**
1. 省錢吧。
1. 開始申請。

### MacOS

1. 開啟新的 **Finder** 視窗
1. 請前往上表中列出的路徑。
1. 右鍵點擊 **plist** 檔案，選擇 **用 Xcode** 開啟>。
1. 在清單頂端新增一個名為 **DisableLicenseWarningPopup 的新金鑰**
1. 將鍵型設為字 **串**
1. 將鍵值設為 **true。**
1. 儲存並關閉檔案。
1. 開始申請。

### Linux

要在 Linux 上設定變數，請遵循以下步驟：

1. 請前往上表中的路徑清單。
1. 打開 **資料夾裡的 .conf** 檔案。
1. 在[一般]行 **下方新增一行**
1. 在新一行，貼上以下文字： **DisableLicenseWarningPopup=true**
1. 存檔。
1. 開始申請。
