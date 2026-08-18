---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/interface/layer-stack/layer-instancing.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中使用圖層實例化，以有效地在多個貼圖集間重複使用圖層。
helpx_creative_field: ""
helpx_description: Painter > Interface > Layer stack > Layer instancing
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 層實例化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 0%

---


# 層實例化

**層實例** 化允許在多個層與 [紋理集](../texture-set/texture-set.md) 間同步圖層參數，同時仍能產生依賴網格的結果。

當建立圖層實例時，原始圖層（或來源圖層）會被用來複製所有現有實例的參數。 **只有原始圖層可以修改**。

>[!WARNING]
>
> 任何繪畫動作（筆觸、多邊形填充等） 只會在來源圖層所在的紋理集上有效。 其他有此圖層實例的貼圖集則會直接捨棄繪製動作。

## 建立圖層實例

要建立圖層實例：

1. 選擇任何現有的圖層
1. 複製圖層（**CTRL+C**）
1. 將它貼上為實例（使用 **CTRL+SHIFT+V** 或右鍵點擊開啟右鍵選單並選擇 **「貼上為實例**」）。

![](../../assets/paste-as-layer-instance.png)

>[!NOTE]
>
> 實例可以從任何層（包括 **群組**）建立。 實例化資料夾可以是一個簡單的方法，可以在不同的材質集上複製多層。 在實例資料夾中新增圖層也會將它們複製到現有實例中。

一旦建立實例，來源圖層與目標圖層會顯示新的圖示。 這個圖示是一個按鈕，可以用來更輕鬆地在來源圖層與其實例間切換，無需手動切換材質集（見下文）。

| 名稱 | 聖像 |
| --- | --- |
| **非實例層** | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/non-instanced.png"/></div> |
| **實例來源** | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/instance-source.png"/></div> |
| **實例目標** | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r3-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/instance-target.png"/></div> |

## 跨材質集建立實例

你可以一次在多個材質集上建立圖層實例，避免手動複製貼上。

要在多個材質集間建立實例：

1. 選擇任何現有的圖層
1. 右鍵點擊該圖層即可開啟右鍵選單
1. 選擇 **跨材質集實例化**
1. 在新視窗中，檢查哪些材質集需要接收實例。
1. 點擊確定以驗證並建立實例。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../assets/instance-across-texture-sets.png)

</td>
<td style="border: 0;" valign="top">

![](../../assets/instance-across-texture-sets-dialog.png)

</td>
</tr>
</table>

>[!NOTE]
>
> 貼圖集名稱旁的驚嘆號表示通道  **不匹配**。 這表示如果在這些材質集中建立了實例，因為它會因為缺少通道而無法正確渲染。

## 在實例與來源間切換

由於實例  **只能**  透過  **編輯原始碼**  來更新（出於技術原因），因此必須選擇來源層來編輯其屬性。\
這可以透過點擊  **圖層堆疊中該圖層的實例屬性按鈕**  來完成。

![](../../assets/instance-properties-optim.gif)

點擊實例屬性按鈕時，它會將屬性視窗&#x200B;**從目前的工具/圖層切換**&#x200B;到&#x200B;**顯示來源圖層及其實例的清單**。\
點擊  **列表中任一元素**  即可自動  **跳轉至此層**  。 這會自動&#x200B;**將目前**&#x200B;選取&#x200B;**的材質集改**&#x200B;成正確的。

使用&#x200B;**實例樹**&#x200B;清單是快速&#x200B;**&#x200B;**&#x200B;從實例到來源，同時同時看到&#x200B;**相依關係**&#x200B;的最佳方式。

## 實例循環（以及如何解決它們）

循環是直接或間接地直接或間接地被用於來源層的實例。 **循環無法被 Substance 3D Painter 引擎計算**，因此必須停用&#x200B;**&#x200B;**，直到修復或移除。

範例：\
![](../../assets/instance-cycle-optim.gif)

在這個範例中，來源層的實例會被移到裡面（因為它是一個資料夾）。 這個實例會出問題，是因為為了產生參數，我們必須從來源查詢參數，而這又取決於實例的參數。 這會形成一個無法自動解決的循環。 該實例會被停用。

唯一能解決這個循環的方法，就是  **把實例移**  出資料夾或  **刪除**  它。

只要實例本身指向不同的來源層，層實例就可以在來源層中使用。
