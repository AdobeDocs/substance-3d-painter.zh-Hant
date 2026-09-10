---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/features/uv-tiles/image-sequence.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中使用帶有 UV 圖塊的影像序列來製作動畫貼圖工作流程。
helpx_creative_field: ""
helpx_description: Painter > Features > UV Tiles > Image Sequence
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 影像序列
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8b892d2d6c9d0f1a3b5d9d3ab9b180a7c2770a83
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# 影像序列

影像序列是一組被歸類為單一資源的影像集合。 影像會根據其檔名中的特定模式被分組在一起。

## 如何將影像匯入序列

匯入影像檔案時，如果檔名符合特定模式，會自動匯入序列。 如果匯入檔案旁邊有其他圖片，也會被納入考量。 因此，不必手動匯入序列中的所有檔案，只需選擇第一個檔案即可。

檔名匹配範例：

以下檔案名稱能成功匯入影像序列，因為它們能辨識檔名最後部分指向 UDIM 編號 1032：

* 檔案\_22.1032.jpg
* 檔案\_22-223.1032.jpg
* 檔案\_22-223-1032.jpg
* 檔案\_22-223\_1032.jpg

以下檔案名稱不會以影像序列匯入，因為它們的結構不正確：

* 檔案\_22-2232032.jpg
* 檔案\_22-223PM2032.jpg
* 檔案\_22-223-0032.jpg
* 檔案\_22-223\_Rec2020.jpg

檔案名稱匹配基於以下正則表達式：

```
 ^(.+?)[\.\-\_](?
```


## 如何使用影像序列

影像序列可以像其他資源一樣載入介面中的任何資源槽。 不過在某些情況下，它們可能需要額外的設定才能正確使用。

在填充圖層（以及填充效果）中[，請確保投影模式設定為&#x200B;**填充（Match Each UV Tile），**&#x200B;以確保序列中的每個影像都被分配到貼圖集中的正確 [UV 圖塊](uv-tiles.md)。](../../painting/fill-projections/fill-projections.md)
