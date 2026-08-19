---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/pipeline-and-integration/configuration/command-lines.html"
breadcrumb-title: ''
description: 學習如何使用 Substance 3D Painter 進行指令列參數的自動化、腳本編寫及管線整合。
helpx_creative_field: ""
helpx_description: Painter > Pipeline and integration > Configuration > Command lines
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 指令列
user-guide-description: ''
user-guide-title: ''
source-git-commit: 22871eab2f25d09bd82f1292d8b3e5f8c4f1c2cf
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---


# 指令列

本頁列出了數個可在啟動應用程式時用於建立或開啟專案的命令列。\
這些命令列可以下方式使用：

```
"Adobe Substance 3D Painter.exe" --command [option] 
```


## 指揮列表

| 指揮 | 說明 |
| --- | --- |
| **——救命**  **——？**   **——h** | 顯示可用命令列的資訊及使用方式。 |
| **--版本**  **-V** | 顯示目前版本的 Substance 3D Painter。 |
| **——網狀** | 用網格載入專案。範例：  `// Create a new project with a specific mesh   "Adobe Substance 3D Painter.exe" --mesh "E:/MymeshFolder/MyMesh.obj"       // Update a mesh inside an existing project   "Adobe Substance 3D Painter.exe" --mesh "E:/MymeshFolder/MyMesh.obj" "E:/MyMeshFolder/Project.spp"` |
| **--網格映射** | 與網格相關的烘焙貼圖（AO、法線、曲率）。 可以多次指定。 命名法：TextureSetName\_AdditionalMapSlot<ul data-preserve-html="true"> <li data-preserve-html="true">環境遮蔽 = <strong> <em> ambient_occlusion </em> </strong></li> <li data-preserve-html="true">曲率 = <strong> <em> 曲率 </em> </strong></li> <li data-preserve-html="true">正規 = <strong> <em> normal_base </em> </strong></li> <li data-preserve-html="true">世界空間標準 = <strong> <em> world_space_normals </em> </strong></li> <li data-preserve-html="true">位置 = <strong> <em> 職位 </em> </strong></li> <li data-preserve-html="true">厚度 = <strong> <em> 厚度 </em> </strong></li> <li data-preserve-html="true">ID = <em> <strong> 身分證 </strong> </em></li> </ul>範例：  `"Adobe Substance 3D Painter.exe" --mesh "E:/MyMeshFolder/MyMesh.obj" --mesh-map " E:/MyMeshFolder/DefaultMaterial_ambient_occlusion.png"` |
| **--由烏迪姆分割** | 為每個 UDIM 磚塊建立一個貼圖集。 |
| **--輸出路徑** | 預設匯出路徑，專案輸出會被匯出。 |
| **--VRAM 預算** | 覆蓋由 Substance 3D Painter 引擎定義的視訊記憶體（VRAM）預算。 「數量」是以兆位元組計算。    範例：  `// Set the VRam budget to 2GB   "Adobe Substance 3D Painter.exe" --vram-budget 2048` |
| **--停用版本檢查** | 啟動時不要檢查是否有新版本的應用程式 |
| **--啟用遠端腳本** | 允許從應用程式外部執行腳本指令。 更多資訊請參見 [「帶有腳本](../../scripting-and-development/scripts-and-plugins/remote-control-with-scripting.md) 的遠端控制」。 |
