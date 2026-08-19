---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/painting/vector-graphic-svg.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中使用向量圖形（SVG 和 AI 檔案）來為貼圖添加可縮放的向量藝術作品。
helpx_creative_field: ""
helpx_description: Substance 3D Painter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 向量圖形（SVG）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---


# 向量圖形（.svg 與 .ai）

![圖片顯示一個 SVG 檔案投影在網格上，旁邊有一串參數](../assets/svg_overview.png)

向量圖形檔案（無論是 <b>.svg</b> 還是 Illustrator <b>.ai</b>）都可以像一般圖片一樣在 Painter 內匯入。 有幾個設定可以調整圖像的外觀，讓它更貼合其他材質。

* 欲了解更多關於 SVG 檔案的資訊，請參閱 [此頁面](https://www.adobe.com/creativecloud/file-types/image/vector/svg-file.html)。
* 欲了解更多關於 AI 檔案的資訊，請參閱 [此頁面](https://www.adobe.com/ie/creativecloud/file-types/image/vector/ai-file.html)。

SVG 和 AI 檔案在圖層堆疊[&#128279;](../interface/layer-stack/layer-stack.md)中使用時（視所選設定而定）會自動轉換成像素影像。這是一個非破壞性的過程，改變解析度或更新原始檔案會相應地更新最終結果。

## 屬性

匯入向量檔案並將其載入圖層或工具屬性後，會有一組參數可用：

| 章節 | 背景設定 | 說明 |
| --- | --- | --- |
| <b>美術白板</b> | <b>美術白板</b> | 選擇檔案中所包含的哪個美術板被使用。  **注意：**  此設定僅適用於 Illustrator （.ai） 檔案。 |
| <b>解決方法</b> | 解決方法 | 定義 svg 在圖層堆疊中用於貼圖時，會轉換成點陣圖影像（像素）的大小。 可能的數值：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>自動</b>：解析度由目前材質集的解析度決定（在填充層/效果中使用時），或在筆刷工具中使用時為 512 像素。<br/> </li> <li data-preserve-html="true"><b>資產</b>：解析度由 SVG 檔案內定義的像素大小決定。<br/> </li> <li data-preserve-html="true"><b>自訂</b>：解析度由介面下方的解析度設定決定。</li> </ul>  <div><img alt="SVG 解析度設定" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_table_row-ad42696-column-7212622_image" src="../assets/svg_resolution_custom.png" title="SVG 解析度設定"/></div> |
|  |  |  |
| <b>作物區域</b> | 裁剪至 | 定義 SVG 形狀如何限制在渲染區域內。 可能的數值：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>資產邊界</b>：面積由 SVG 檔案內定義的邊界所定義。</li> <li data-preserve-html="true"><b>自訂</b>：該區域由下方介面設定中明確定義的數值。<br/> </li> </ul> |
|  | 方形寬高比 | 若裁切區域由 <b>資產邊界</b>定義，此設定可確保原始比例保留，避免在將 SVG 渲染為方形影像時出現錯誤拉伸。 這種設定會讓某些元素意外地顯現。 為了避免這個問題，請關閉這個設定，改為在填充圖層/效果中手動調整 UV 設定。 |
|  | 左上角 右下角 | 如果裁切 的 are 設為自訂區域，這些設定允許手動定義區域，透過指定左上角和右下角。 |
|  |  |  |
| <b>範圍</b> | 範圍 | 在渲染 SVG 檔案前，先定義包含哪些元素。 它預設為 <b>Document</b>，代表 SVG 檔案的所有內容都會被使用。 使用 <b>「變更</b> 」按鈕調整要包含哪些元素。 |

### 範圍視窗

當編輯向量圖的範圍（見上述設定）時，會出現一個視窗，列出元素以指定要從最終渲染影像中加入或排除的元素。

使用 <b>「顯示縮圖</b> 」的檢查框來顯示每個元素的圖片。

![](../assets/v10_ai_thumbs.jpg)
