---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/features/plugins/autosave.html"
breadcrumb-title: ''
description: 學習如何使用 Substance 3D Painter 中的自動儲存插件，定期自動儲存專案。
helpx_creative_field: ""
helpx_description: Painter > Features > Plugins > Autosave
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 自動存檔
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---


# 自動存檔

![](../../assets/autosave-details.png){width="500px"}

自動儲存插件允許  **建立目前已開啟專案的備份**  。 它會在旁邊建立一個檔案，同時保持目前專案不變。

備份檔案將位於三個可能的位置：

* 如果目前專案已經被儲存，備份就會放在旁邊。
* 如果專案從未被儲存（未命名），備份會放在使用者文件資料夾的自動儲存資料夾。 （  **文件/寓言/Substance 3D 畫家/自動存檔**  ）
* 如果已啟用覆寫設定，備份會位於設定中指定的路徑中。

*介面中有一個貪睡按鈕可用來延遲自動存檔。*

## 自動存檔是怎麼觸發的？

自動存檔是基於內部計時器，計時器結束後自動存檔流程開始。\
貪睡按鈕會在計時器快結束時自動啟動，讓自動存檔延遲幾分鐘。

所有基於時間的數值都可以透過設定視窗修改。

## 如何關閉自動存檔？

如果需要關閉自動存檔，可以透過插件選單來操作。 要做到這點，請點選&#x200B;**自動儲存**>**的插件**>**停用**&#x200B;選單。

## 設定自動存檔

要設定自動存檔行為，請點選  **「插件**  」>  **自動存檔**  >  **設定**  選單。

* **自動存檔間隔（分鐘**  ）：標示每次自動存檔之間等待多久。
* **自動存檔檔案**  數量：為特定專案所建立的備份檔案數量。
* **貪睡間隔：**  點擊貪睡鍵時自動存檔會延遲多久。
* **存檔前的警告時間：**  在自動存檔觸發前，貪睡按鈕啟動且進度條可見前，還有多久。

>[!NOTE]
>
> 自動存檔計時器會在以下情況下暫停：
> 
> * 引擎正在進行運算
> * 材質正在匯出
> * 設定視窗已開啟
> * 該計畫目前正在被保存

視窗底部可以覆寫備份檔案的預設位置。\
當啟用「  **Always save in the following directory**  」這個設定時，所有備份檔案都會在指定的資料夾裡（預設路徑是使用者的文件資料夾）。
