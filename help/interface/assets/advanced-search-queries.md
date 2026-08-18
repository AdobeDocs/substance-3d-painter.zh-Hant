---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/interface/assets/advanced-search-queries.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中建立進階搜尋查詢，利用複雜的搜尋條件尋找特定素材。
helpx_creative_field: ""
helpx_description: Painter > Interface > Assets > Advanced search queries
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 進階搜尋查詢
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---


# 進階搜尋查詢

進階搜尋查詢允許你構建複雜的搜尋，並將其作為 [已儲存的搜尋](saved-searches.md)重複使用。

進階查詢可在搜尋欄中使用，並可包含以下內容

1. **路徑**  ：允許依資料夾結構細化搜尋結果。
1. **使用**  ：列出應用程式中所有可能的使用方式
1. **文字查詢**  ：允許自由新增任何其他類型的查詢（例如自訂關鍵字）

在定義新搜尋查詢時，允許多重選擇。

## 路徑

路徑查詢允許根據路徑細化查詢。 **「路徑篩選**」面板列出所有可用的函式庫（你可以透過編輯>設定>函式庫自行新增）。\
你可以利用路徑定義來依自訂函式庫路徑或階層中的特定子資料夾來篩選。

## 使用情況

使用定義什麼是資源，以及如何在 Substance 3D Painter 中使用它。 有些可以依資源的檔案類型來定義。\
舉例來說——

* **pbr.glsl**：一個著色器檔案——只能當作著色器使用，不能用其他用途。
* **effect.sbsar**：一個物質檔案——它可以是產生器、過濾器，甚至是材質，因此如果原始圖形（在 Designer 中）沒有設定它的使用，使用者必須在匯入時於 Painter 中標示。

## 文字

文字查詢支援多種篩選方式，有些比一般介面更進階。\
只要輸入正確的關鍵字即可啟用這些功能。

* **可用的搜尋類型**  ：
  * 「  **N：**  」：姓名
  * “  **s：**  ” ： 書架/圖書館（包含「session」與「project」）
  * 「  **p：**  」：路徑
  * 「  **u：**  」：用法
* **逃脫**  ：可以在需要逃脫的角色前加上「**\**  」，或用引號代替，例如：
  * **一個名字\ 加空格**
  * **「一個帶空格的名字」**
* **特定屬性（或群組）：**  若要搜尋特定屬性，請在「或群組」前加上型別指定符。 範例：
  * **n，b，c，d:a**：名字是 a 或 b 或 c 或 d
* **搜尋行為**  ：
  * 為了篩選特定用法，請在搜尋中加入特定  **關鍵字**  ，例如：「  **images**  ambient」
  * 若要新增多個請求，請使用逗號 “  **，**  ”，例如：「cobalt  **，**  gold」（如果使用逗號，搜尋只會顯示同時符合兩個關鍵字的資源）
  * 要搜尋確切姓名，請使用驚嘆號「！」 最後，舉例：  **DI！**  （會回傳髒土&#x200B;**但不會**&#x200B;回傳&#x200B;**&#x200B;**&#x200B;滴落，關鍵字會關閉模糊匹配）
  * 要排除某個模式，請使用連字號 “  **-**  ”，例如 ：  **u:image n：-normal**  （會回傳不含「normal」的圖片）
* **匹配功能（模式後綴）：**
  * **預設**  ：近似匹配（模糊）
  * **包含**  ：！
  * **正則表達式**  ：#
  * **相等**  ： =
  * **以 ： ^ 開頭**
  * **以 ： &amp; 結尾**
