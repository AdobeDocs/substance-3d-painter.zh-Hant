---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/features/color-management.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中設定色彩管理，確保整個工作流程的色彩準確度一致。
helpx_creative_field: ""
helpx_description: Painter > Features > Color management
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 色彩管理
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 0%

---


# 色彩管理

![](../../assets/banner-cm-doc.jpg)

色彩管理是指色彩的處理與轉換。 從匯入資源到螢幕上顯示顏色，最後匯出材質。 色彩校正對於確保不同應用呈現一致的視覺效果非常重要。

在應用程式中，色彩管理透過整合 [OpenColorIO](https://opencolorio.org/) （簡稱 OCIO）第二版來處理。 OCIO 是電影與動畫中轉換與顯示色彩的標準技術。 要啟用色彩管理，只要建立新專案或開啟現有專案並啟用專用設定即可。

>[!NOTE]
>
> 色彩管理自 7.4.0 版本起提供。

## 專案設定

色彩管理設定：

* [Adobe ACE - ICC 的色彩管理](color-management-with-adobe-ace-icc.md)
* [OpenColorIO 的色彩管理](color-management-with-opencolorio.md)

## 詞彙

了解幾個與色彩管理相關的技術術語，有助於更好地理解相關工作流程：

| 關鍵詞 | 說明 |
| --- | --- |
| **色彩空間** | 定義顏色的座標系統。 |
| **工作空間** | 應用程式內部用來混合紋理、上色等的色彩空間。 |
| **顯示轉換** | 顯示轉換將工作空間的線性色彩轉換到螢幕的色彩空間，以感知方式顯示人眼所見的顏色。 顯示轉換通常包含色調映射通道，用以壓縮顏色以符合螢幕允許的有限數值範圍。 |
| **配置** | 一個 OCIO 設定檔。 它定義了工作空間、色彩空間清單以及顯示變換清單。 |
| **王牌** | ACES 代表 Academy Color Encoding System，是許多數位影像檔案交換應用中的標準。 此標準預設包含兩個版本。 |
| **音色映射** | 這是將色彩值從 HDR（高動態範圍）映射到 LDR（低動態範圍）的過程。 此過程有助於近似多種顏色的顯示。 |

## 色彩管理頻道列表

在應用程式內部，哪些通道是色彩管理的，哪些不是（資料/直通）是預先定義好的。

| 頻道 | 是色彩管理嗎 |
| --- | --- |
| **環境遮蔽** | 不 |
| **逆向角** | 不 |
| **各向異性能級** | 不 |
| **底色** | **是的** |
| **混合遮罩** | 不 |
| **毛色** | **是的** |
| **毛色正常** | 不 |
| **毛皮不透明度** | 不 |
| **毛髮粗糙度** | 不 |
| **被殼鏡面水平** | 不 |
| **彌漫** | **是的** |
| **遷移** | 不 |
| **光澤** | 不 |
| **高度** | 不 |
| **Ior** | 不 |
| **金屬** | 不 |
| **正常** | 不 |
| **不透明度** | 不 |
| **反思** | 不 |
| **粗糙度** | 不 |
| **散射** | 不 |
| **散射色彩** | **是的** |
| **光澤色** | **是的** |
| **光澤不透明度** | 不 |
| **光澤粗糙度** | 不 |
| **鏡面鏡面** | **是的** |
| **鏡面邊緣顏色** | **是的** |
| **鏡面層級** | 不 |
| **半透明** | 不 |
| **透射式** | **是的** |
| **UserX（0-15）** | 這取決於 [貼圖集的設定](../../interface/texture-set/texture-set-settings.md)。 預設情況下，使用者頻道並非色彩管理。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r31-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/user-demo.png"/></div> |

## 色彩選擇器

啟用色彩管理時， [色彩選擇器的](../../interface/color-picker.md) 行為會略有改變：

* 顏色會根據目前選擇的顯示器進行編輯。
* 介面中加入了一些額外資訊。

欲了解更多資訊，請參閱色彩選擇器 [文件頁面](../../interface/color-picker.md)。

## 視窗控制

2D 與 3D 視圖皆為色彩管理，且視窗頂端有專用設定可控制使用哪種顯示變換：

![](../../assets/viewport-cm.png)

* **左鍵**：啟用或停用視窗的顯示轉換。 如果關閉，視窗會顯示顏色為原始/直通。 這個按鈕預設是啟用的。
* **右側下拉選單**：指定要用哪個顯示變換來轉換顏色並顯示在螢幕上。 預設值是基於 OCIO 設定。 這個設定不會隨專案儲存，因為它可能依賴於監控器。

>[!NOTE]
>
> 在單獨模式（單獨觀看頻道）中，當觀看資料頻道時，色彩管理會自動關閉（詳見上方列表）。

## 匯出設定

主要的匯出設定是由專案設定（見上文）所驅動。

在匯出材質](../../export/export.md)視窗中[，有一個關鍵字可以用來附加檔案名稱中每個材質所使用的色彩空間：**$colorSpace**。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../assets/export-list-1.png){width="320px"}

</td>
<td style="border: 0;" valign="top">

![](../../assets/export-list-2.png){width="500px"}

</td>
</tr>
</table>

## 覆寫色彩空間

可能需要指定一個替代色彩空間，讓資源與預設值不同。 這可以透過色彩空間選單來完成。

### 改變資源的色彩空間

在屬性視窗](../../interface/properties.md)內[，是否可以覆寫特定資源的色彩空間（目前該資源的使用位置）。

要做到這點，請展開色彩空間區塊，並使用下拉選單指定新的色彩空間：

![](../../assets/color-space-menu.png)

### 改變環境貼圖的色彩空間

在顯示設定中[啟用&#x200B;**覆蓋環境地圖色彩空間**，然後在列表中選擇與資源相符](../../interface/display-settings/display-settings.md)的色彩空間。

![](../../assets/color-sace-menu-env.png)
