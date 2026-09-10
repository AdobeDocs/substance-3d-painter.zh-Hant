---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/features/automatic-uv-unwrapping.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中使用自動 UV 展開，自動生成 3D 模型的 UV 佈局。
helpx_creative_field: ""
helpx_description: Painter > Features > Automatic UV Unwrapping
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 自動紫外線展開
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 0%

---


# 自動紫外線展開

![](../assets/auto-unwrap-update-810.jpg)\
自動 UV 展開功能允許在匯入 3D 模型時自動產生 UV 島。 它可以用來繪製沒有任何現有 UV 的 3D 模型。

## 啟用自動 UV 展開功能

![](../assets/uv-new-project.png)

建立新專案或重新匯入網格到現有專案時，請確保勾選了「自動展開」這個設定。 如果停用，這個流程會被跳過，網格 UV 會保持不變。

## UV 展開設定

![](../assets/unwrap-settings.png)

在匯入網格並使用展開過程時，可以使用以下設定。 部分設定可透過介面中的選項按鈕進行。

| 章節 | ***背景設定*** | ***描述*** |
| --- | --- | --- |
| **展開序列** | **接縫** | 控制接縫（UV 島邊界）是否應該只為沒有接縫或總是重新生成的網格產生。可能的數值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong> 產生缺失資料 </strong> （預設）：缺少缺失的網格會產生接縫。</li><li data-preserve-html="true"><strong> 重新計算所有 </strong> ：所有網格都會產生接縫。</li></ul> |
| **紫外線島** | 控制 UV 展開是否應該從沒有 UV 的網格產生，或是針對任何網格產生。 可能的數值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong> 產生缺失資料 </strong> （預設）：會針對缺少的 UV 網格產生 UV 展開。</li><li data-preserve-html="true"><strong> 重新計算所有 </strong> ：所有網格都會產生 UV 展開。</li></ul> |  |
| **打包** | 控制網格 UV 島嶼的打包與佈局。可能的數值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong> 產生缺失資料 </strong> （預設）：為缺少 UV 的網格打包 UV 島。</li><li data-preserve-html="true"><strong> 重新計算所有 </strong> ：打包所有UV島。</li></ul> |  |
|  |  |  |
| **版面自訂** | **邊際大小** | 定義了紫外線島之間的間距。 此設定會以與解析度無關的一般百分比。可能的數值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong> 無邊際 </strong> ： 0%</li><li data-preserve-html="true"><strong> 小型 </strong> （預設）：0.2%</li><li data-preserve-html="true"><strong> 中等： </strong> 0.5%</li><li data-preserve-html="true"><strong> 大型： </strong> 1%</li></ul> |
|  | **紫外線島的方向** | 在包裝過程中控制紫外線島的方向。可能的數值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>無約束</strong> （預設）：計算方向時不施加約束。</li><li data-preserve-html="true"><strong>對齊 3D 網格</strong>：將 UV 島嶼限制為朝向網格方向</li></ul> |
|  |  |  |
| **UV瓷磚** | **UV磚的最大數量** | 如果啟用 UV Tiles 工作流程，這些設定會決定最大要產生的圖塊數量，以分配到 UV 島嶼上。 |
|  |  |  |
| **最佳化** | **避免使用拉長的紫外線島** | 若啟用此程序，將被認為過長的 UV 島拆分，以提升材質空間的使用效率。前（上）與下後（下）的例子： <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r10-column-c2_dynamic_grid_items_grid-cell_position-par_image" src="../assets/uv-before-after.jpg" width="400px"/></div> |

## 已知限制

以下是與展開過程相關的限制清單：

* 處理高多邊形網格可能需要很長時間。
* 完全相同座標的頂點會合併
* 在某些罕見情況下，UV 生成可能會在某些網格部分失敗
* 在某些情況下，單一紫外線島的紋素比率不均勻或高度扭曲
* 貼圖集間非均勻的紋素比
* 產生的 UV 島可能非常拉長，在某些情況下無法放入 UV 空間
* 退化面或非三角形網格面且邊緣小或重疊，可能無法展開 UV
