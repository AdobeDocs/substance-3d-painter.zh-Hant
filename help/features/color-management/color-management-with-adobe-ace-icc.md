---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/features/color-management/color-management-with-adobe-ace-icc.html"
breadcrumb-title: ''
description: 學習如何在Substance 3D Painter中使用Adobe ACE和ICC色彩管理，以維持穩定的色彩工作流程。
helpx_creative_field: ""
helpx_description: Painter > Features > Color management > Color management with Adobe ACE - ICC
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Adobe ACE - ICC 的色彩管理
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---


# Adobe ACE - ICC 的色彩管理

本頁列出與 Adobe Color Engine（ACE）相關的色彩管理設定，用於使用 ICC 設定檔的影像。

## 專案設定

![](../../assets/cm-ace.png)

專案設定可在新專案視窗建立新專案[&#128279;](../../getting-started/project-creation.md)時設定，或使用[專案設定](../../interface/project-configuration.md)視窗設定。

>[!NOTE]
>
> 如果載入環境變數（見下文）或預設檔案，介面中的設定將會被停用。

可用的設定如下：

| 章節 | 背景設定 | 說明 |
| --- | --- | --- |
| **配置** | **色彩管理** | 定義用哪個引擎來管理顏色。可能的數值：<ul data-preserve-html="true"> <li data-preserve-html="true"><strong>舊有</strong> （預設）：使用預設的 sRGB/Linear sRGB 伽瑪色彩校正。</li> <li data-preserve-html="true"><strong>OpenColorIO</strong>：使用 OCIO 整合。</li> <li data-preserve-html="true"><strong>Adobe ACE</strong>：Adobe 色彩引擎，以支援 ICC 設定檔。</li> </ul> |
|  | **使用預設檔案** | 如果啟用了，允許透過 JSON 設定檔來存取色彩管理設定。 |
|  | **預設檔案** | 預設檔案的路徑，以 json 格式呈現。 更多細節請見下方。 |
|  |  |  |
| **色彩設定** | **工作色彩空間** | 引擎在應用程式內部使用的色彩空間。 這是紋理可轉換成（匯入）或從（匯出）的色彩空間。可能的值有：<ul data-preserve-html="true"> <li data-preserve-html="true"><strong>線性 sRGB IEC61966-2.1</strong> （預設）</li> <li data-preserve-html="true"><strong>ACEScg ACES 工作空間 AMPAS S-2014-004</strong></li> <li data-preserve-html="true"><strong>線性 Adobe RGB（1998）</strong></li> </ul> |
|  | **呈現意圖** | 請指定用於在色彩空間間轉換顏色的方法。可能的數值：<ul data-preserve-html="true"> <li data-preserve-html="true"><strong>知覺</strong></li> <li data-preserve-html="true"><strong>飽和度</strong> （預設）</li> <li data-preserve-html="true"><strong>相對半音階</strong></li> <li data-preserve-html="true"><strong>絕對半音階</strong></li> </ul> |
|  |  |  |
| **點陣圖匯入色彩空間預設值** | **8 位元影像** | 匯入 8 位元影像檔案時預設使用的色彩空間。 |
|  | **16位元影像** | 匯入 16 位元影像檔案時預設使用的色彩空間。 |
|  | **浮點影像** | 匯入 HDR/EXR 影像檔案時預設使用的色彩空間。 |
|  | **如有內嵌 ICC 設定檔（建議）使用。** | 如果啟用了，請使用圖片檔案中的 ICC 設定檔來調整顏色。 |
|  |  |  |
| **物質材料** | **材質色彩空間預設** | 定義 Substance 材質的色彩管理輸入/輸出要用哪種色彩空間。 |
|  |  |  |
| **匯出色彩空間** | **8 位元影像** | 匯出 8 位元影像檔案時預設使用的色彩空間。 |
|  | **16位元影像** | 匯出 16 位元影像檔案時預設使用的色彩空間。 |
|  | **浮點影像** | 匯出 HDR/EXR 影像檔案時預設使用的色彩空間。 |

## 使用預設檔案

![](../../assets/cm-ace-env-var.png)

建立新專案時，可以使用預設檔案（json 格式）來驅動 ACE 設定。

### 環境變數

環境變數 **PAINTER\_ACE\_CONFIG** 可用來指定預設檔案的路徑。 如果有，應用程式會一直使用預設檔案來驅動色彩管理設定。 介面中的設定會被關閉。

更多細節請參閱 [環境變數](../../pipeline-and-integration/configuration/environment-variables.md) 頁面。

### 預設範例

以下是一個可用作預設檔案的 json 檔案範例：

```
{ 

  "color settings": { 

    "working color space": "Linear Adobe RGB (1998)", 

    "rendering intent": "Saturation" 

  }, 

  "bitmap import color space defaults" : { 

    "8 bit images": "image P3", 

    "16 bit images": "image P3", 

    "floating point images": "Raw", 

    "use embedded ICC profiles when available": false 

  }, 

  "substance material": { 

    "material color space default": "image P3" 

  }, 

  "export colors spaces" : { 

    "8 bit images": "image P3", 

    "16 bit images": "image P3", 

    "floating point images": "Raw" 

  } 

} 
```
