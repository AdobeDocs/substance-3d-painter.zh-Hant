---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/pipeline-and-integration/resource-management/adding-resource-paths-by-editing-preferences-manually/editing-resource-paths-manually.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 偏好設定中手動編輯資源路徑，以自訂你的資源架位置。
helpx_creative_field: ""
helpx_description: Painter > Pipeline and integration > Resource management > Adding resource paths by editing preferences manually > Editing resource paths manually
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 手動編輯資源路徑
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---


# 手動編輯資源路徑

本頁是關於如何在不啟動應用程式的情況下編輯偏好設定以新增或移除資源路徑的指南。

## 偏好位置

資源位置由應用程式偏好管理，這些偏好可能會根據桌面形式而改變：

<table data-preserve-html="true"> <colgroup> <col/> <col/> <col/> </colgroup> <tbody> <tr> <th>系統</th> <th>版本</th> <th>路徑</th> </tr> <tr> <td rowspan="2"><p><strong>窗戶</strong></p><p>（登記處）</p></td> <td><strong>7.2</strong> 或更新版本</td> <td>HKEY_CURRENT_USER\Software\Adobe\Adobe Substance 3D Painter</td> </tr> <tr> <td>遺產</td> <td>HKEY_CURRENT_USER\軟體\寓言\物質畫家</td> </tr> <tr> <td rowspan="2"><p><strong>麥克</strong></p><p>（圖書館）</p></td> <td><strong>7.2</strong> 或更新版本</td> <td>/使用者/[用戶名]/Library/偏好設定/com.adobe.Adobe Substance 3D Painter.plist</td> </tr> <tr> <td>遺產</td> <td>/使用者/[使用者名稱]/Library/Preferences/com.substance3d.Substance Painter.plist</td> </tr> <tr> <td rowspan="2"><strong>Linux</strong></td> <td><strong>7.2</strong> 或更新版本</td> <td>/home/[username]/.config/Adobe/Adobe Substance 3D Painter.conf</td> </tr> <tr> <td>遺產</td> <td>/home/[username]/.config/Allegorithmic/Substance Painter.conf</td> </tr> </tbody> </table>

## 在 Windows 上新增路徑

在 Windows 上，路徑可透過 Windows 登錄檔管理：

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../assets/reg-shelf-pathinfos.png)

</td>
<td style="border: 0;" valign="top">

![](../../../assets/reg-content.png)

</td>
</tr>
</table>

1. 點擊  **開始>執行**  或按下  **Windows + R**  。
1. 在對話框中輸入「**regedit**」（不加引號）並按  **確定**。
1. 在登錄檔編輯器&#x200B;**視窗左側**&#x200B;的樹狀檢視中導航，並前往上述登錄檔金鑰。
1. **在 pathInfos** 下方&#x200B;**加入一個帶有**&#x200B;數字&#x200B;**作為名稱的鑰匙**。根據現有的按鍵（從 1 開始）增加數量。
1. **右鍵點擊**&#x200B;視窗右側>**新的**>**字串值**。將它 **命名為停用**  ，並將值設為 **false**。
1. **右鍵點擊**&#x200B;視窗右側>**新的**>**字串值**。命名並&#x200B;**&#x200B;**&#x200B;輸入自訂書架名稱。
1. **右鍵點擊**&#x200B;視窗右側>**新的**>**字串值**。命名為 **路徑**  ，並將數值設為書架所在的路徑。
1. 別忘了將「pathInfos **」中的**「**大小**」鍵加1。
1. 關窗。
1. 開始申請。

可以透過將可寫的 Shelf **條目**&#x200B;值改為新位置名稱，將新路徑定義為預設路徑（如預設）。

![](../../../assets/default-shelf.png)

## 在 Linux 上新增路徑

在 Linux **上**，可以透過儲存在主目錄中的使用者應用程式偏好設定檔建立額外的路徑（參見。

1. 引導你走上前面提到的路徑。
1. 打開 Substance 3D Painter.config 這個檔案&#x200B;**&#x200B;**
1. 往下滑到 **[書架]** 區塊

透過遞減最後可見的數字來新增書架路徑，例如：

```
pathInfos2disabled=false  

pathInfos2name=custom_resources 

pathInfos2path=/home/Username/Documents/custom_path 

writableShelf=custom_resources
```


使用  **writableShelf**  變數指定哪條路徑會是預設路徑（例如新資源，例如預設）。

儲存變更並重新啟動應用程式。
