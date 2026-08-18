---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/workflow-issues/project-issues/a-project-has-been-processed-as-a-text-file-and-is-now-corrupted.html"
breadcrumb-title: ''
description: 學習如何恢復已處理成文字檔的損壞 Substance 3D Painter 專案檔案。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Workflow Issues > Project Issues > Corrupted project file
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 專案檔案損壞
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# 一個專案被處理成文字檔，現在已經損壞

有時載入專案時會出現以下錯誤：

```
[Hdf5Archive] Archive 'project.spp' appears to have been processed as a text file and is irremediably corrupted. 

[Project management] The selected project 'project.spp' isn't valid!
```


此錯誤表示專案已在 Substance 3D Painter 外被修改，無法  **正確**  回讀。\
這通常是在版本控制軟體（例如  **Perforce**  ）將 Substance 3D Painter 專案  **處理成文字檔而非二進位檔**  時發生。 唯一的解決方法是在版本控制軟體中新增一條規則/例外，強制以二進位&#x200B;**格式處理** spp 檔案。欲了解更多 Perforce **相關**&#x200B;資訊，請參閱專門文件：<https://www.perforce.com/perforce/r16.1/manuals/cmdref/p4_typemap.html>
