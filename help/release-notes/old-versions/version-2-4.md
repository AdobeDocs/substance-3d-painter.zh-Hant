---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/release-notes/old-versions/version-2-4.html"
breadcrumb-title: ''
description: 查看 Substance 3D Painter 2.4 版本的發布說明，了解新功能、改進與錯誤修正。
helpx_creative_field: ""
helpx_description: Painter > Release notes > Old versions > Version 2.4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 版本 2.4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 0%

---


# 版本 2.4

**Substance Painter 2.4** 著重於提升書架窗口及資源管理。

上映日期： *2016年10月27日*

## 主要特色

### 新置物架窗戶，配備先進過濾功能

![](../../assets/new-shelf-240.jpg)

新的書架視窗提供了 **更好的資源組織** ，並 **提供了全新的內容**&#x200B;過濾方式。 我們新增了自訂 **預設** 的功能，每個預設都有自己的篩選功能（方便快速切換不同查詢）。 這些預設也可以&#x200B;**獨立到新視窗**，讓&#x200B;**書架有多個視角，而不只是像以前那樣只有一個。**&#x200B;過濾功能也提供了 **瀏覽磁碟**&#x200B;資料夾階層的方式，對於細化較一般的查詢非常方便。 我們也改進 **了右鍵點擊資源時的右鍵選單** ，以提供 **更實用的資訊**。

如需建立進階查詢，請參閱文件中專門的部分： [進階搜尋查詢](../../interface/assets/advanced-search-queries.md)

### 新的匯入資源視窗

![](../../assets/import-window-240.png)

隨著書架的重製，我們也 **改善了資源匯入視窗**。 視窗現在更一致，可以用 **三種不同方式** 呼叫：透過檔案選單、書架視窗中的按鈕，或像之前一樣，將資源拖放到書架視窗中。 新視窗允許&#x200B;**你快速設定多個資源**&#x200B;的使用量&#x200B;**&#x200B;**，這表示你不必再先拖放資源到正確位置。我們也新增了自訂 **路徑** 以建立子資料夾的功能，以利用新的樹狀檢視功能。

更多細節請參閱文件中專門的部分： [透過匯入視窗新增資源](https://helpx.adobe.com/tw/substance-3d/unlisted/documentation/spdoc/adding-content-via-the-import-window-151584824.html)

### 新粒子預設

![](../../assets/particle-240.png)

我們 **重新調整** 了之前 **的粒子預設** ，使其更易於使用（尤其是 **雨** 的預設）。 我們也藉此 **機會加入了帶有新行為的新預設** ：來看看 **Electric Circuit、Electric Lines、Rococo 和 Veins Small** ！

## 教學

新書架的功能和用途已在我們最新的教學中介紹：

## 發行說明

### 2.4.1

（2016年10月28日發行）

**已修正：**

* 使用範本建立專案時會當機
* 在匯出過程中關閉匯出對話框時會當機
* [Mac]儲存專案時出現錯誤（匯出預設未儲存）
* [書架]建立新預設會顯示兩次
* [書架]預設在沒有管理員權限的情況下無法以唯讀模式載入

### 2.4.0

（2016年10月27日發行）

**新增：**

* [書架]新的介面可瀏覽資源（樹狀檢視、篩選器等）
* [書架]允許將搜尋儲存為預設
* [書架]允許從預設建立新視窗
* [書架]新匯入資源介面
* [書架]不要複製文件資料夾裡預設的寓言書架
* [書架]新粒子預設：電路、電線、洛可可、小脈絡
* [書架]改良舊粒子預設，使其更易於使用（如「Rain」）
* [書架]新增資源情境選單資訊
* [視窗]載入環境地圖時提升效能
* [視窗]新增非二的冪次方環境地圖支援

**已修正：**

* 摘下面罩時的撞擊聲
* 儲存預設後上色時當機
* 某些顯示卡會因環境模糊而當機
* 當用迷你架子指派錯誤資源時會當機
* [書架]清理 + 儲存 移除專案中資源的標籤與元資料
* [Shelf] 匯入預設會在書架上顯示其資源
* [匯出]從高度通道產生的法線貼圖強度較低
* [匯出]網格的法線不一定會出現在最終法線貼圖中
* [匯出]有時候透明的膨脹會導致沒有透明
* [腳本操作]「alg.plugin\_root\_directory」可以回傳截斷的網路路徑
* [貼圖集]重新開啟非方形專案時會啟用鎖定按鈕
