---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/features/uv-reprojection.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中使用 UV 重投影，將貼圖在不同 UV 佈局間轉移。
helpx_creative_field: ""
helpx_description: Painter > Features > UV Reprojection
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 紫外線重投影
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 0%

---


# 紫外線重投影

UV 重投影是當你更改材質解析度或匯入新網格時自動發生的過程。\
如果你在文件中載入新的網格（透過  [專案設定](https://substance3d.adobe.com/display/draftpainter/project%20configuration)  視窗），你所有的動作都會重新投影到那個新網格上。 拓撲是否改變（只要相似）或 UV 是否改變並不重要。 由於重投影是透過重新計算所有圖層和筆觸來運作，這可能會花一些時間（尤其是在高材質解析度下）。

2D 繪圖

由於 2D 視圖中的每一筆劃都是在 UV 空間中執行，若重新匯入後網格的 UV 大幅改變，無法正確重新投影。 讓你的專案重新投影proof（proof）最好的方法是依賴ID貼圖的遮罩和其他選取和繪製，而不是用3D視圖。

## 重投影是怎麼運作的？

Substance 3D Painter 會將資料儲存在世界空間的 3D 空間，以確保一切不破壞。 這表示當重新匯入網格時，Substance 3D Painter 會嘗試繪製在重新匯入前的網格位置，無法知道某些零件可能移動的位置。

另外，當 Substance 3D Painter 匯入網格時，它會計算包圍框來登錄空間，並為工具（畫筆、粒子等）定義相對比例。 這個包圍盒在每個軸上都是 1 單位寬。 當你匯入新網格時，如果你取消勾選「保留筆劃」，我們會重新將邊界框歸一化成新網格。 因此，如果你的網格大小大幅改變，筆劃是可以移動的。 不過如果你勾選「保留筆觸」，我們會將原本的邊界框縮放到新的框上，以便正確地重新投影筆觸。

>[!WARNING]
>
> 改變 3D 網格的單位可能會導致 UV 重投影無法正常運作;舊網格和新網格即使拓撲沒有改變，也可能被解讀為截然不同的縮放。 理想狀況下，避免更換設備配置，因為這可能很難修復。
