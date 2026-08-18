---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/release-notes/old-versions/version-2017-2.html"
breadcrumb-title: ''
description: 請參閱 Substance 3D Painter 2017.2 版本的發行說明，了解新功能、改進與錯誤修正。
helpx_creative_field: ""
helpx_description: Painter > Release notes > Old versions > Version 2017.2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 版本 2017.2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---


# 版本 2017.2

**Substance Painter 2017.2** 透過 Anchor Point 系統引入了一項強大的新功能。 它允許在層堆疊中建立更進階的配置，開啟許多新的可能性。

發行日期： *2017年7月27日*

## 主要特色

### 新錨點效應

![](../../assets/anchor-height-blend-optim.gif)

**Substance Painter 新增了一種效果類型** ，除了既有 **的 Filter** 和 **Level** 之外，現在你也能找到新的 **Anchor 點**。 這個新效果允許在圖層堆疊中定義一個&#x200B;**位置**&#x200B;**，然後在**&#x200B;專案的其他圖層中互相引用&#x200B;**。**&#x200B;這讓例如可以將圖層的高度資訊應用到該圖層上方的遮罩中，讓混合更自然（如上方 gif 所示）。

由於錨點作為一種效果運作，可以在多種情況下產生&#x200B;**：**&#x200B;圖層內容&#x200B;**、**&#x200B;遮罩&#x200B;**，甚至作為**&#x200B;通透&#x200B;**&#x200B;**&#x200B;濾波器。即使該圖層被關閉，效果效果仍然有效。 請注意，錨點只定義一個位置，並未定義你能從中取得的資訊。 這些資訊是在建立錨點參考的地方所定義的。

欲了解更多技術細節與範例，請參閱專屬頁面： [Anchor Point](../../features/effects/anchor-point.md)

### 多項新改良

除了新的錨點效應外，我們還參與了：

* 可以重新命名某些效果，例如填充和繪畫
* 新增腳本功能，允許與其他應用程式如 Unity 建立即時連結

## 教學

新功能詳情請見我們最新的影片：

## 發行說明

### 2017.2

（2017年7月27日發行）

**新增：**

* [效果]新增可進行圖層與遮罩參照的錨點
* [圖層]能重新命名填充與繪製效果
* [外掛]更新後的物質來源外掛
* [腳本]允許查詢紋理集解析度
* [腳本執行]允許取得繪畫引擎的狀態
* [效能]改良的專案載入與刷刷沖壓優化

**已修正：**

* [工具]調整材料參數時的效能問題
* [引擎]解析度變更時筆觸消失（4K>2K）
* [3D 視圖]切空間與 baker 不同步
* [書架]使用者文件中的書架路徑不會自動建立
* [書架]更新後讓預設與先前版本相容
* [著色器]非 PBR 著色器已經無法運作了
* [烘焙師]啟用「按姓名配對」時，ID 地圖烘焙失敗
* [範例]認識 Mat 範例專案貼圖集名稱有誤
* 在建立範本前儲存專案會回傳寫入權限錯誤
