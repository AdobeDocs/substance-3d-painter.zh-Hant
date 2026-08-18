---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/interface/texture-set/texture-set-reassignment.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中重新指派貼圖集，以重新組織網格指派和貼圖貼圖。
helpx_creative_field: ""
helpx_description: Painter > Interface > Texture Set > Texture Set reassignment
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 材質集重新指派
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 0%

---


# 材質集重新指派

![](../../assets/txtset-reassignment-window.png)

貼圖集重新指派視窗允許將圖層堆疊指派調整到場景網格的不同部分。 這在匯入新網格到現有專案後，某些材質集被禁用時非常有用。 這是因為圖層堆疊被分配給一個已經不存在的材質。 透過重新指派視窗，可以恢復該圖層堆疊（詳見下方「恢復停用的貼圖集」）。

要進入貼圖集重新分配視窗，請進入 [貼圖集清單](texture-set-list.md) 視窗，選擇 **設定>重新分配貼圖集**。

窗戶分為三個部分：

* **停用的材質集** ：列出目前未使用的材質集。
* **專案貼圖集** ：列出目前所有指派給網格材質的貼圖集。
* **網格材質** ：列出專案的網格材質。

視窗還有額外的按鈕，可以執行以下動作：

* **復原** ：還原到視窗的先前狀態
* **重做** ：重新套用你已撤銷的變更。
* **套用** ：關閉視窗並執行重新指派。
* **取消** ：關閉視窗並丟棄正在進行的變更。

## 重新指派貼圖集

![](../../assets/reassign-existing-sets.gif)

重新指派貼圖集可以透過簡單的拖放按鈕來完成。

## 恢復停用的材質集

![](../../assets/reassign-disabled-sets.gif)

當貼圖集不再與網格材質相關聯時，可以被停用。\
這種情況可能發生在將新網格匯入專案時，因為專案和新網格的材質名稱不同。

要還原貼圖集，只需&#x200B;**在「**&#x200B;專案貼圖集&#x200B;**」列表中將貼圖集的位置與其中一個交換**&#x200B;即可。

## 刪除已停用的貼圖集

![](../../assets/reassign-delete-sets.gif)

點擊「停用材質集&#x200B;**」中貼圖集**&#x200B;旁的&#x200B;**叉號**&#x200B;會&#x200B;**標記刪除**&#x200B;該貼圖。\
刪除會在點擊 **視窗底部的「套用** 」按鈕時發生。

>[!WARNING]
>
> 這個動作一旦用「套用」按鈕關閉視窗，就無法撤銷。
