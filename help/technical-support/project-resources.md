---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/project-resources.html"
breadcrumb-title: ''
description: 取得 Substance 3D Painter 的專案資源與技術文件，以提升您的工作流程與故障排除。
helpx_creative_field: ""
helpx_description: Substance 3D Painter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 專案資源
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---


# 專案資源與環境

管理專案資源有助於為您的專案在 Painter 中的表現奠定良好基礎。

+++縮細烘焙貼圖
有時候並非所有烘焙的地圖都需要 2k 或 4k 解析度。 別猶豫先用 2K 烘焙一批，然後用較低解析度重新烘焙，看看視覺上是否有差異。

+++

+++管理匯入的點陣圖
匯入的影像會大幅影響效能，因此要注意匯入內容。 如果你的材質集設定為 2k，且不會以更高解析度匯出，使用 8k 影像不會有正面影響——它的品質會被限制在 2k，因為那是材質集的解析度。

格式也很重要——EXR、HDR 甚至 PNG 都比 JPG 重很多，而且並非所有影像都需要 EXR 那樣的品質（例如底色與高度細節）。

+++

+++調整著色器設定
超高光畫質會帶來更準確的效果，但設定成本很高。 著色器同時啟用的效果越多，計算就越複雜。 如果可能，將複雜材質拆分到另一個有獨立著色器的材質集。 如果位移是啟用的，請注意鑲嵌參數。

+++

+++調整檔案選項
使用 <b>檔案>儲存>儲存並縮減檔案</b> <b>用 size </b>來清除不需要的資料，並使用 <b>Remove unused 資源</b> 來移除匯入到專案、且在專案內未被使用的檔案。

+++
