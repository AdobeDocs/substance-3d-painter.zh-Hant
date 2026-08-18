---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/workflow-issues/shelf-issues/font-import.html"
breadcrumb-title: ''
description: 學習如何修復 Substance 3D Painter 中字型檔案匯入問題，以成功匯入並使用字型資源。
helpx_creative_field: ""
helpx_description: Substance 3D Painter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 字型檔案無法匯入
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---


# 字型檔案無法匯入

隨著文字資源](../../../painting/text-resource.md)的引入[，字型檔案會在啟動時自動收集。字型檔案也可以手動匯入。

在這些情況下，可能會出現幾個錯誤訊息：

* 當拖放檔案到 Painter 介面時，
* 當 Painter 在磁碟上發現字型時（圖書館爬取）。

## 如何解決這個問題

如果出現檔案 <b>損壞</b>的錯誤訊息，試著找其他版本，Painter&#39;s 可能能載入。 請注意，目前僅 <b>支援.ttf</b> 和 <b>.otf</b> 格式。

若出現授權 <b>問題</b>的錯誤訊息，表示該字型與 Painter 不相容，無法匯入。

### 訊息概述

|  |  |
| --- | --- |
| <b>錯誤訊息</b> | <b>說明</b> |
| 「LIBRARYNAME」函式庫中存在影響四個字型檔案的問題：FONTNAME、FONTNAME、FONTNAME,... | 此訊息收集了一份已識別出無法在 Painter 中匯入的字型檔名的簡短清單。 這些檔案會被忽略，且不會出現在資產視窗中。 |
| 發現字型問題。 詳情請見 https://... | 一則通用訊息表示字型出現問題。 |
| 因為 FONTNAME 的授權限制，無法匯入。 詳情請見 https://... | Painter 需要能夠將字型嵌入專案檔案才能使用。 不允許的字型（在他們的元資料中指定）因此無法被匯入。 |
| 無法匯入 FONTNAME，因為檔案損壞或是不支援的類型。 詳情請見 https://... | Painter 無法讀取提供的字型檔案。 |
