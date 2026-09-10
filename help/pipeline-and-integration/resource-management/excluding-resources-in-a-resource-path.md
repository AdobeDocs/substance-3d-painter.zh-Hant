---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/pipeline-and-integration/resource-management/excluding-resources-in-a-resource-path.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中排除特定資源，以改善書架組織。
helpx_creative_field: ""
helpx_description: Painter > Pipeline and integration > Resource management > Excluding resources in a resource path
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 排除資源路徑中的資源
user-guide-description: ''
user-guide-title: ''
source-git-commit: 22871eab2f25d09bd82f1292d8b3e5f8c4f1c2cf
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 0%

---


# 排除資源路徑中的資源

本頁說明如何設定忽略檔案，指定在資產視窗爬取過程中[&#128279;](../../interface/assets/assets.md)會被忽略的資源和資料夾。這可以避免不必要的資源被展示。

>[!NOTE]
>
> 此功能自 7.2.3 版本起提供。

## 建立忽略檔案

導航到你想隱藏資源的資源資料夾位置。 接著建立一個名為以下的檔案：

```
.ignore_assets_pt
```


>[!NOTE]
>
> 請注意，檔名必須以點開頭。

完成後應該是這樣的樣子：

![](../../assets/ignore-file-location.png)

## 範例

以下檔案內容將捨棄除預設函式庫資料夾以外的所有資源與資料夾：

```
## exclude all

* 

 

## re-include library directories

!alphas 

!colorluts 

!effects 

!emitters 

!environments 

!export-presets 

!generators 

!materials 

!presets 

!procedurals 

!receivers 

!shaders 

!smart-masks 

!smart-materials 

!templates 

!textures
```


## 規則與指引

下表展示了適用於忽略檔案的一般規則。

>[!NOTE]
>
> 忽略檔案的模式匹配是大小寫區分的，獨立於作業系統的行為。

| 統治 | 說明 | 範例 |
| --- | --- | --- |
| **空白線** | 空行且不符合任何內容。 可用作可讀性的分隔符。 |  |
| **目錄分隔符** | 前斜線用作目錄分隔符。 分離符可能出現在搜尋模式的開始、中間或結束處。如果在模式的開頭或中間（或兩者）有分隔符，那麼該模式相對於忽略檔案本身的目錄層級是相對於的。 否則，該模式也可能在忽略檔案層級以下的任何層級匹配。 如果模式末尾有分隔符，該分隔符會被忽略，模式仍會匹配檔案和目錄。 | `folder/filename.extension   folder/sub-folder` |
| **留言欄** | 以數字符號（或雜湊值）開頭的行作為註解。 | `# This is a comment` |
| **星號** | 星號則是對應除前斬以外的任何東西。 | `# Match anything starting with Alpha   alpha*   # Match any file with given extension   *.jpg` |
| **角色範圍** | 字元範圍可在括號間指定，以匹配資料夾與檔名。<ul data-preserve-html="true"> <li data-preserve-html="true"><b>[abc]</b>：匹配給定列表中的一個角色</li> <li data-preserve-html="true"><b>[a-c]</b>：匹配給定範圍內的一個字元</li> <li data-preserve-html="true"><b>[！abc]</b>：配對一個不在指定列表中的角色</li> <li data-preserve-html="true"><b>[！a-c]</b>：配對一個不在指定範圍內的字元</li> </ul>範圍和列表也可以是數字，格式為 <b>[0-9]。</b> | `# Exclude any UDIM image in PNG   *_[0-9][0-9][0-9][0-9].png` |
| **逃脫角色** | 標示那些原本會被忽略或用作規則的字面字元。 | `# This is a comment   [#]This/Is/A/Path` |
| **後方格** | 後方格子會被忽略，除非能逃脫。 | `# Match a subfolder with trailing space   folder/subfolder[ ]` |
| **驚嘆前綴** | 在圖案前加上驚嘆號可以使其無效。任何先前模式排除的匹配檔案都會重新被包含。 若排除該檔案的父目錄，則無法重新包含該檔案。 為了效能考量，爬行不會列出被排除的目錄，所以無論檔案在哪裡定義，任何包含檔案上的模式都不會影響它們。 | `# Re-include specific file   !my_file_name.png` |
