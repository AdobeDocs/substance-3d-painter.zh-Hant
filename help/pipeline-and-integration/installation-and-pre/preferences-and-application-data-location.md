---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/pipeline-and-integration/installation-and-preferences/preferences-and-application-data-location.html"
breadcrumb-title: ''
description: 了解 Substance 3D Painter 的偏好設定與應用程式資料位置，以管理設定與使用者資料。
helpx_creative_field: ""
helpx_description: Painter > Pipeline and integration > Installation and preferences > Preferences and application data location
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 偏好設定與應用程式資料位置
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 1%

---


# 偏好設定與應用程式資料位置

本頁彙整了各版本與平台應用程式偏好設定儲存位置的資訊。\
知道偏好設定存放在哪裡會很有用，以備你想新增 **自訂架** （用於工作室安裝）或移除這些偏好設定以執行 **乾淨安裝** 應用程式。

## 偏好設定

這條路徑是應用程式偏好設定的位置（儲存的捷徑、書架/資產路徑、介面佈局等）。

<table data-preserve-html="true"><colgroup> <col/> <col/> <col/> </colgroup><tbody><tr><th>系統</th><th>版本</th><th>路徑</th></tr><tr><td rowspan="2"><p><strong>窗戶</strong></p><p>（登記處）</p></td><td><strong>7.2</strong> 或更新版本</td><td>HKEY_CURRENT_USER\Software\Adobe\Adobe Substance 3D Painter</td></tr><tr><td>遺產</td><td>HKEY_CURRENT_USER\軟體\寓言\物質畫家</td></tr><tr><td rowspan="2"><p><strong>麥克</strong></p><p>（圖書館）</p></td><td><strong>7.2</strong> 或更新版本</td><td>/使用者/[用戶名]/Library/偏好設定/com.adobe.Adobe Substance 3D Painter.plist</td></tr><tr><td>遺產</td><td>/使用者/[使用者名稱]/Library/Preferences/com.substance3d.Substance Painter.plist</td></tr><tr><td rowspan="2"><strong>Linux</strong></td><td><strong>7.2</strong> 或更新版本</td><td>/home/[username]/.config/Adobe/Adobe Substance 3D Painter.conf</td></tr><tr><td>遺產</td><td>/home/[username]/.config/Allegorithmic/Substance Painter.conf</td></tr></tbody></table>

## 應用資料

這條路徑是額外應用程式資料（資產縮圖、日誌檔等）的位置。

<table data-preserve-html="true"><colgroup> <col/> <col/> <col/> <col/> </colgroup><tbody><tr><th>平台</th><th>版本</th><th colspan="2">路徑</th></tr><tr><td rowspan="4"><strong>窗戶</strong></td><td rowspan="2"><strong>7.2</strong> 或更新版本</td><td colspan="1">App Data（本地）</td><td colspan="1">C：\Users\[username]\AppData\Local\Adobe\Adobe Substance 3D Painter</td></tr><tr><td colspan="1">App Data（漫遊）</td><td colspan="1">C：\Users\[username]\AppData\Roaming\Adobe\Adobe Substance 3D Painter</td></tr><tr><td rowspan="2">遺產</td><td colspan="1">App Data（本地）</td><td colspan="1">C：\Users\[用戶名]\AppData\Local\Allegorithmic\Substance Painter</td></tr><tr><td colspan="1">App Data（漫遊）</td><td colspan="1">C：\Users\[用戶名]\AppData\Roaming\Allegorithmic\Substance Painter</td></tr><tr><td rowspan="2"><strong>麥克</strong></td><td colspan="1"><strong>7.2</strong> 或更新版本</td><td colspan="2">/使用者/[使用者名稱]/函式庫/應用程式支援/Adobe/Adobe Substance 3D 畫家</td></tr><tr><td colspan="1">遺產</td><td colspan="2">/使用者/[使用者名稱]/函式庫/應用程式支援/寓言/內容畫家</td></tr><tr><td rowspan="2"><strong>Linux</strong></td><td colspan="1"><strong>7.2</strong> 或更新版本</td><td colspan="2">/home/[username]/.local/share/Adobe/Adobe Substance 3D 畫家</td></tr><tr><td>遺產</td><td colspan="2">/home/[username]/.local/share/寓意/Substance Painter</td></tr></tbody></table>

>[!NOTE]
>
> 上述路徑中的部分目錄可能預設是隱藏的。 在檔案總管手動輸入路徑，或顯示隱藏檔案以查看。
