---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/features/effects/anchor-point.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中使用錨點效果，參考其他圖層的材質，進行進階合成。
helpx_creative_field: ""
helpx_description: Painter > Features > Effects > Anchor Point
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 錨點
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 0%

---


# 錨點

錨點是一種可以暴露圖層堆疊中任意資源或元素，並在圖層堆疊的不同區域以不同目的及調整方式參照的方法。 它們開啟了全新的可能性，讓你能有效地連結圖層或遮罩，並讓單一錨點影響專案的多個面向，將 Substance 3D Painter 轉化為真正的非線性體驗。

>[!NOTE]
>
> 錨點只能在已建立的相同貼圖中被參考。 在材質集之間無法建立錨點與其參考之間的連結。

## 新增錨點

Anchor Point 可在效果選單中取得。 它們可以加在圖層和遮罩上。

![](../../assets/add-anchor-point.png)

## 用錨點作為參考

錨點可以被另一層參考：這會將錨點的內容實例化到參考它的圖層中。

錨點可作為以下資源的參考資料：

* 填充層
* 填充效應
* 物質過濾器的輸入（效果、程序、產生器）

![](../../assets/anchor-point-resource.png)

只有位於參考圖層下方&#x200B;**的錨點**&#x200B;才能作為參考。\
如果你把錨點移到指向它的圖層上方，就會破壞參考。 如果你想取消這個動作，可以還原。

![](../../assets/layer-broken.png)![](../../assets/reference-broken.png)

## 尋找錨點的參考資料

當你點擊錨點時，可以在屬性中看到該錨點作為參考的圖層清單。

![](../../assets/references.png)

## 找到錨點

當你是以 Anchor Point 作為參考的填充圖層/效果時，你可以跳到錨點。

![](../../assets/jump-to-anchor-point.png)
