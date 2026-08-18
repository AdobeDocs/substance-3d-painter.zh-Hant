---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/technical-issues/miscellaneous-issues/corrupted-texture-error-message.html"
breadcrumb-title: ''
description: 學習如何修復 Substance 3D Painter 中損壞的貼圖錯誤訊息，以恢復貼圖功能。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Miscellaneous Issues > Corrupted texture error message
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 材質錯誤訊息損壞
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---


# 材質錯誤訊息損壞

專案中的材質損壞會導致儲存過程中失敗，甚至導致專案完全損壞且無法修復。 不過這可以手動修正。\
當開啟專案時，日誌中會出現類似此錯誤訊息的資源損壞：

![](../../../assets/corrupt1.png)

## 修復損毀的資源參考

### 1 - 尋找資源

錯誤出現的第一步是找出並識別有問題的資源。\
大多數情況下，問題來自 **Mesh 貼圖** （烘焙材質）。 一個快速驗證的方法就是查看圖層堆疊中的遮罩產生器。

損壞的資源會長這樣：

![](../../../assets/corrupt2.png)

>[!NOTE]
>
> 這也可能意味著該資源根本不見了。\
> 為了確定，可以試著清空槽位並手動重新影響烘焙。 如果紅十字縮圖還在，代表資源已經損壞。

### 2 - 替換資源

要替換損壞的資源，必須先移除所有相關參考資料。 如果電流相對較小，也可以手動完成。\
然而，如果專案跨越多個材質集或多層， [資源更新器](../../../features/plugins/resources-updater.md)可以協助找到損壞的資源，並暫時替換成另一個資源。

>[!NOTE]
>
> * 在烘焙材質的外殼裡，別忘了也清空 Texture Set](../../../interface/texture-set/texture-set-settings.md) 視窗裡[的 Mesh Maps 欄位。
> * 只在貼圖集設定中使用的烘焙，例如法線貼圖，也可能因此損壞。 如果錯誤依舊，也試著移除它們。

### 3 - 清理

當所有損壞資源的參考資料都消失後，從主選單執行專案清理（**檔案** > **清理**）。\
這樣應該會移除專案中所有未被使用的損壞資源。 你可以透過瀏覽書架上的專案分頁來確認所有有問題的資源都已經移除。

### 4 - 存檔

清理完成後，試著儲存專案：

* 如果儲存時沒有錯誤，專案就不再損壞（網格地圖現在可以重新烘焙和資源重新匯入）。
* 如果錯誤仍然存在，代表專案中仍有對損毀資源的參考。
