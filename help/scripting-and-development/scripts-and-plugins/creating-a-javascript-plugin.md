---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/scripting-and-development/scripts-and-plugins/creating-a-javascript-plugin.html"
breadcrumb-title: ''
description: 學習如何為 Substance 3D Painter 建立 JavaScript 外掛，以擴展功能並自動化自訂工作流程。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > Scripts and plugins > Creating a Javascript plugin
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 建立 Javascript 外掛
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---


# 建立 Javascript 外掛

這份逐步指南說明如何建立一個簡單的外掛，讓它能匯出專案中目前選取圖層的遮罩。

本指南中插件的目標是將專案中目前 Texture Set 的所有通道匯出為獨立的材質。

## 1 - 前往 plugins 資料夾

要新增 Javascript 外掛，必須在 Substance 3D Painter 的外掛資料夾中建立一個資料夾。

要進入 **plugins** 資料夾，請前往：

<table data-preserve-html="true" style="width: 100.0%;"> <colgroup> <col style="width: 15.0%;"/> <col style="width: 15.0%;"/> <col style="width: 70.0%;"/> </colgroup> <tbody> <tr> <th>平台</th> <th>版本</th> <th>路徑</th> </tr> <tr> <td rowspan="2"><strong>窗戶</strong></td> <td><strong>7.2</strong> 或更新版本</td> <td colspan="1">C：\Users\username\Documents\Adobe\Adobe Substance 3D Painter</td> </tr> <tr> <td colspan="1">遺產</td> <td colspan="1">C：\Users\username\Documents\Allegorithmic\Substance Painter</td> </tr> <tr> <td rowspan="2"><strong>麥克</strong></td> <td colspan="1"><strong>7.2</strong> 或更新版本</td> <td colspan="1">/使用者/使用者名稱/文件/Adobe/Adobe Substance 3D 畫家</td> </tr> <tr> <td colspan="1">遺產</td> <td colspan="1">/使用者/用戶名/文件/寓言/內容畫家</td> </tr> <tr> <td rowspan="2"><strong>Linux</strong></td> <td colspan="1"><strong>7.2</strong> 或更新版本</td> <td colspan="1">/首頁/用戶名/文件/Adobe/Adobe Substance 3D 畫家</td> </tr> <tr> <td>遺產</td> <td colspan="1">/首頁/用戶名/文件/寓言/內容畫家</td> </tr> </tbody> </table>

### 2 - 建立插件資料夾

外掛名稱是根據其父資料夾名稱來命名的。

在這個例子中，只要在 plugins 資料夾裡建立一個名為  **export-textures**  的新資料夾。

### 3 - 建立外掛檔案

打開新建立的資料夾，建立兩個空白的文字檔（記事本）：

* **main.qml**
* **toolbar.qml**

qml 檔案副檔名是一種用於為 Qt QML 語言所建立腳本的 Javascript 擴充功能。 它不僅能執行 Javascript 程式碼，也能建立自訂使用者介面。

**main.qml** 檔案是必須的，它是應用程式用來載入插件時會先尋找的檔案。不過，也可以建立任意名稱的額外檔案，讓腳本能拆分成多個部分，方便管理。 在這種情況下，  **toolbar.qml**  會用來描述外掛在介面中新增按鈕的外觀。

### 4 - 劇本內容

將腳本檔案打開文字編輯器，如 Notepad++，並貼上以下程式碼片段。 可以看看程式碼註解以獲得更多細節。

**toolbar.qml**

```
import QtQuick 2.7 

import AlgWidgets 2.0 

import AlgWidgets.Style 2.0 

 

AlgButton 

{ 

 tooltip: "" 

 iconName: "" 

 text: "Export Textures" 

}
```


**main.qml**

```
// Default includes, to acces Qt/QML 

// and Substance 3D Painter APIs 

import QtQuick 2.7 

import Painter 1.0 

 

// Root object for the plugin 

PainterPlugin 

{ 

 // Disable update and server settings 

 // since we don't need them 

 tickIntervalMS: -1 // Disabled Tick 

 jsonServerPort: -1 // Disabled JSON server 

 

 // Implement the OnCompleted function 

 // This event is used to build the UI 

 // once the plugin as been loaded by Substance 3D Painter 

 Component.onCompleted: 

 { 

  // Create a toolbar button 

  var InterfaceButton = alg.ui.addToolBarWidget("toolbar.qml"); 

 

  // Connect the function to the button 

  if( InterfaceButton ) 

  { 

   InterfaceButton.clicked.connect( exportTextures ); 

  } 

 } 

 

 // Custom function called by the Button, 

 // this is the core of the plugin 

 function exportTextures() 

 { 

  // Catch errors in the script during execution 

  try 

  { 

   // Verify if a project is open before  

   // trying to export something 

   if( !alg.project.isOpen() ) 

   { 

    return; 

   } 

 

   // Retrieve the currently selected Texture Set (and sub-stack if any) 

   var MaterialPath = alg.texturesets.getActiveTextureSet() 

   var UseMaterialLayering = MaterialPath.length > 1 

   var TextureSetName = MaterialPath[0] 

   var StackName = "" 

 

   if( UseMaterialLayering ) 

   { 

    StackName = MaterialPath[1] 

   } 

 

   // Retrieve the Texture Set information 

   var Documents = alg.mapexport.documentStructure() 

   var Resolution = alg.mapexport.textureSetResolution( TextureSetName ) 

   var Channels = null 

 

   for( var Index in Documents.materials ) 

   { 

    var Material = Documents.materials[Index] 

 

    if( TextureSetName == Material.name ) 

    { 

     for( var SubIndex in Material.stacks ) 

     { 

      if( StackName == Material.stacks[SubIndex].name ) 

      { 

       Channels = Material.stacks[SubIndex].channels 

       break 

      } 

     } 

    } 

   } 

 

   // Create the export settings 

   var Settings = { 

    "padding":"Infinite", 

    "dithering":"disbaled", // Hem, yes... 

    "resolution": Resolution, 

    "bitDepth": 16, 

    "keepAlpha": false 

   } 

 

   // Build the base of the export path 

   // Files will be located next to the project 

   var BasePath = alg.fileIO.urlToLocalFile( alg.project.url() ) 

   BasePath = BasePath.substring( 0, BasePath.lastIndexOf("/") ); 

 

   // Export the each channel 

   for( var Index in Channels ) 

   { 

    // Create the stack path, which defines the channel to export 

    var Path = Array.from( MaterialPath ) 

    Path.push( Channels[Index] ) 

 

    // Build the filename for the texture to export 

    var Filename = BasePath + "/" + TextureSetName 

 

    if( UseMaterialLayering ) 

    { 

     Filename += "_" + StackName 

    } 

 

    Filename += "_" + Channels[Index] + ".png" 

 

    // Perform the export 

    alg.mapexport.save( Path, Filename, Settings ) 

    alg.log.info( "Exported: " + Filename ) 

   } 

  } 

  catch( error ) 

  { 

   // Print errors in the log window 

   alg.log.exception( error ) 

  } 

 } 

} 
```


完成後，儲存並關閉檔案。

### 5 - 載入並啟用外掛

啟動 Substance 3D Painter，預設新插件會自動載入並啟用。

打開一個專案，然後點擊外掛建立的 UI 按鈕，匯出目前選取的材質集通道：

![](../../assets/button-plugin.png)

要啟用或停用外掛，請使用介面頂端的 Javascript 選單：

![](../../assets/disable-plugin.png)
