---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/pipeline-and-integration/resource-management/adding-saved-searches-manually.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中手動新增已儲存的搜尋，以快速存取常用資源篩選器。
helpx_creative_field: ""
helpx_description: Painter > Pipeline and integration > Resource management > Adding saved searches manually
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 手動新增已儲存的搜尋
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---


# 手動新增已儲存的搜尋

資產搜尋查詢（或儲存搜尋）可以透過編輯設定檔來定義。 本頁說明了相關方法。

## 設定檔的位置

若要新增自訂儲存的查詢，請前往使用者的 Documents 資料夾並開啟 **Shelf.ini** 檔案。

<table data-preserve-html="true" style="width: 100.0%;"> <colgroup> <col style="width: 15.0%;"/> <col style="width: 15.0%;"/> <col style="width: 70.0%;"/> </colgroup> <tbody> <tr> <th>平台</th> <th>版本</th> <th>路徑</th> </tr> <tr> <td rowspan="2"><strong>窗戶</strong></td> <td><strong>7.2</strong> 或更新版本</td> <td colspan="1">C：\Users\username\Documents\Adobe\Adobe Substance 3D Painter</td> </tr> <tr> <td colspan="1">遺產</td> <td colspan="1">C：\Users\username\Documents\Allegorithmic\Substance Painter</td> </tr> <tr> <td rowspan="2"><strong>麥克</strong></td> <td colspan="1"><strong>7.2</strong> 或更新版本</td> <td colspan="1">/使用者/使用者名稱/文件/Adobe/Adobe Substance 3D 畫家</td> </tr> <tr> <td colspan="1">遺產</td> <td colspan="1">/使用者/用戶名/文件/寓言/內容畫家</td> </tr> <tr> <td rowspan="2"><strong>Linux</strong></td> <td colspan="1"><strong>7.2</strong> 或更新版本</td> <td colspan="1">/首頁/用戶名/文件/Adobe/Adobe Substance 3D 畫家</td> </tr> <tr> <td>遺產</td> <td colspan="1">/首頁/用戶名/文件/寓言/內容畫家</td> </tr> </tbody> </table>

## 範例

以下是可放入設定檔的內容範例：

```
[filters] 

size=4 

1name=Grunge 

1query="u:basematerial=,smartmaterial=,smartmask=,texture=,procedural=,brush=,alpha= grunge" 

2name=Procedural 

2query="u:procedural=" 

3name=Environment 

3query="u:environment=" 

4name=Default Filters 

4query="p:/allegorithmic/^ u:filters="
```


語法運作方式如下：

* **Size**： 決定應用程式需要讀取並載入的自訂預設數量。
* **數字**：行首定義其當前目標預設（例如：  **1/**）。
* **查詢**（數字後）定義實際使用的搜尋詞。 在範例中，它使用  **u：**  表示用法，  **p：**  表示路徑，或用字串表示搜尋詞。 查詢內容必須用引號包裹。 欲了解可用詞彙，請參閱 [此頁面](../../interface/assets/advanced-search-queries.md)。
* **名稱**：預設的名稱。
