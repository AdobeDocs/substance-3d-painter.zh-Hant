---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/interface/texture-set/texture-set-list.html"
breadcrumb-title: ''
description: 學習如何使用 Substance 3D Painter 中的貼圖集清單，管理並組織專案中的多個貼圖集。
helpx_creative_field: ""
helpx_description: Painter > Interface > Texture Set > Texture Set list
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 材質組合清單
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 0%

---


# 材質組合清單

![](../../assets/texture-set-list.png)

貼圖集合列表&#x200B;**視窗**&#x200B;會顯示專案中目前 3D 模型的所有材質 ID。它允許切換並查看模型中每個材質的圖層堆疊及其專用設定。

貼圖集合列表視窗的主要目標是允許從一個材質切換到另一個材質，以存取每個材質所對應的圖層堆疊。\
以材質分層工作流程為例[，**子堆疊**&#x200B;會顯示&#x200B;**在材質集名稱下方**。](../../features/dynamic-material-layering.md)

>[!WARNING]
>
> 一次只能編輯或繪製一個材質集。

## 材質集狀態

貼圖集可以有多種狀態：

![](../../assets/txtset-status.png)

* **已選取** ：目前正在編輯的材質集。 選擇材質集會相應更新 [圖層堆疊](../layer-stack/layer-stack.md) 和 [著色器設定](../shader-settings/shader-settings.md) 視窗。
* **可見/隱藏** ：更多細節請見下方可見性章節。
* **停用** ：這表示貼圖集及其相關的圖層堆疊無法附加到網格中的材質上。 更多資訊請參閱 [貼圖集重新指派](texture-set-reassignment.md) 。

## 可見度

![](../../assets/texturesetlist.png)

材質集的顯示可由專用圖示管理：

| *聖像* | *行動* | *描述* |
| --- | --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/txtsetlist-icon-menu.png"/></div> | 開啟選單 | 開啟一個新選單，執行以下操作：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>全部顯示</strong>：將在視窗中顯示所有貼圖集。</li><li data-preserve-html="true"><strong>全部隱藏</strong>：會隱藏視口中的所有材質集。</li><li data-preserve-html="true"><strong>反轉顯示/隱藏</strong>：可見的貼圖集會變成隱藏，隱藏的貼圖集也會變得可見。</li></ul> |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/txtsetlist-icon-isolate.png"/></div> | 專注模式 | 在此模式下，隔離目前啟用的材質集，並隱藏其他所有材質集。 再次點擊此按鈕即可退出模式。 |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r3-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/txtsetlist-icon-visible.png"/></div> | 可見度 | 點擊 Texture Set 旁邊的按鈕，可以在視窗中隱藏或顯示 Texture Set。 |

>[!NOTE]
>
> 預設情況下，繪製&#x200B;**時**&#x200B;只會顯示正在選取的貼圖集。你可以在 [偏好設定](../settings/settings.md) 中取消勾選「**僅顯示繪製**&#x200B;時選取的材質」來改變此行為。\
> 注意：在上色 **時隱藏其他貼圖集可以提升效能**。

## 情境選單

![](../../assets/txtset-list-contextualmenu.png)

當右鍵點擊貼圖集名稱時，會開啟一個包含以下操作的情境選單：

* **顯示/隱藏貼圖集** ：切換貼圖集的可見性（如前一節所述）
* **編輯名稱** ：允許重新命名材質集。 這個名稱也會在材質匯出過程中使用。 也可以透過雙擊 Texture Set 名稱來重新命名。
* **將名稱重設為 \*original name\*** ：如果網格材質中原本的材質名稱已被更改，請恢復原有的材質集名稱。
* **編輯描述** ：允許新增或更改與貼圖集相關的描述。

## 著色器管理

每個材質集名稱右側的按鈕可用來管理著色器指派。\
預設情況下，每個貼圖集共用同一個著色器實例。 不過有時候只針對網格的特定部分使用不同的著色器會比較方便。 你可以點擊按鈕並選擇「**新著色器實例**」。 接著，在 [著色器設定](../shader-settings/shader-settings.md) 視窗中，可以更改著色器及其參數，而不會影響其他貼圖集。

![](../../assets/capture-d-e-cran-2018-07-12-a-15-45-32.png){width="500px"}

## 設定

設定按鈕開啟一個新選單，顯示多個操作：

* **隱藏空描述** （預設）：若為空，則隱藏描述欄位
* **隱藏所有描述** ：即使描述欄位不是空的，也要隱藏
* **顯示所有描述：** 即使描述欄位為空，也顯示
* **匯入著色器參數** ：允許匯入 json 檔案以設定貼圖集的著色器參數
* **重新指派貼圖集** ：更多資訊請參閱 [貼圖集重新指派](texture-set-reassignment.md) 。
