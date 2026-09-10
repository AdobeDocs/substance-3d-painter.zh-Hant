---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/pipeline-and-integration/resource-management/preferences-and-content-migration.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中遷移偏好與內容，以升級或遷移至新系統。
helpx_creative_field: ""
helpx_description: Painter > Pipeline and integration > Resource management > Preferences and content migration
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 偏好與內容遷移
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---


# 偏好與內容遷移

本頁說明如何將資料從偏好設定和 Shelf/Assets 遷移到新版本中使用。

在 7.2 版本釋出後，偏好設定和書架位置已調整，以便在多個版本的應用程式（Substance 3D 獨立版、Steam 和 Creative Cloud Desktop 版）中通用。 這項變更意味著先前的偏好設定和自訂資源 **現在預設會被忽略** （**但不會遺失**）。 由於書 **架** 已更名為 **資產**，遷移過程包含以下幾個步驟。

## 遷移的架子與資產資源

預設使用者的資源位置已改變，導致原本放在文件資料夾中的內容現在會被新版本的應用程式忽略。 要恢復這些內容，只需將檔案從一個位置移到另一個位置即可。

### 內容在哪裡可以找到

書架或資產路徑可在以下地點找到：

<table data-preserve-html="true" style="width: 100.0%;"><colgroup> <col style="width: 15.0%;"/> <col style="width: 15.0%;"/> <col style="width: 70.0%;"/> </colgroup><tbody><tr><th>平台</th><th>版本</th><th>路徑</th></tr><tr><td rowspan="2"><strong>窗戶</strong></td><td><strong>7.2</strong> 或更新版本</td><td colspan="1">C：\Users\username\Documents\Adobe\Adobe Substance 3D Painter</td></tr><tr><td colspan="1">遺產</td><td colspan="1">C：\Users\username\Documents\Allegorithmic\Substance Painter</td></tr><tr><td rowspan="2"><strong>麥克</strong></td><td colspan="1"><strong>7.2</strong> 或更新版本</td><td colspan="1">/使用者/使用者名稱/文件/Adobe/Adobe Substance 3D 畫家</td></tr><tr><td colspan="1">遺產</td><td colspan="1">/使用者/用戶名/文件/寓言/內容畫家</td></tr><tr><td rowspan="2"><strong>Linux</strong></td><td colspan="1"><strong>7.2</strong> 或更新版本</td><td colspan="1">/首頁/用戶名/文件/Adobe/Adobe Substance 3D 畫家</td></tr><tr><td>遺產</td><td colspan="1">/首頁/用戶名/文件/寓言/內容畫家</td></tr></tbody></table>

### 如何遷移書架內容

舊的 Shelf 內容只是硬碟上的檔案，所以遷移它們只是把這些檔案放到正確的位置。

1. 關閉申請
1. 前往舊的 Shelf 資料夾
1. 複製或剪掉子資料夾（alpha、程序檔、材質等）
1. 前往新的資產資料夾
1. 將你之前複製的子資料夾貼到資產資料夾裡，如果被要求覆蓋就覆蓋。

現在重新啟動應用程式，內容應該會出現在資產視窗裡。

>[!NOTE]
>
> 記得要複製子資料夾，而不是只複製資源的父資料夾。 父資料夾已經從 Shelf **改名**&#x200B;為 **assets**，所以只複製父資料夾不會讓應用程式看到資源。

### 如何遷移 Shelf 預設

架式預設會儲存在設定檔中。 要遷移這些預設：

1. 關閉申請
1. 前往舊的 Shelf 資料夾
1. 複製或剪掉Shelf.ini檔案
1. 前往新的資產資料夾
1. 貼上檔案並覆寫現有檔案

現在重新啟動應用程式，儲存的搜尋應該會出現在專用區塊或資產視窗中。

## 遷移偏好

我們建議你從介面手動重新調整應用程式設定。 這是最安全的方式來遷移資訊，且不會引發相容性問題。

否則，請參考以下頁面了解偏好設定現在的位置： [偏好設定與應用程式資料位置](https://helpx.adobe.com/tw/substance-3d/unlisted/documentation/spdoc/application-preferences-location-147095594.html)。
