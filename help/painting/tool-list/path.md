---
helpx_url: 'https://helpx.adobe.com/substance-3d-painter/painting/tool-list/path.html'
breadcrumb-title: ''
description: 使用 Substance 3D Painter 中的路徑工具來建立和編輯路徑，進行精準的貼圖繪製與筆觸放置。
helpx_creative_field: ''
helpx_description: Painting > Path tools list > Path tool
helpx_experience_level: ''
helpx_learn_topic: ''
helpx_tags: ''
title: 路徑工具概述
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6fcf10add7086a0e2a070ee6046c0a261ef1ae34
workflow-type: tm+mt
source-wordcount: '1666'
ht-degree: 0%

---


# 路徑工具概述

![圖片顯示鞋子上使用的路徑工具](../../assets/v90_banner_path.jpg)

**路徑工具**&#x200B;允許你定義一條曲線，並在網格表面設置點。曲線建立後，不同的路徑工具允許你沿著曲線創造不同的效果。

## 建立路徑

路徑可以在繪圖層和繪圖效果上建立。 有兩種方式可以存取路徑工具：

* **透過介面**：從左側進入工具列，點擊倒數第三個圖示。
* **透過鍵盤快捷鍵：預設工具沒有指定快捷鍵**。 這可以透過在設定選單中編輯「選擇沿路徑繪製工具」的快捷鍵來更改。

選擇工具後，可以在 3D 視口中點擊 3D 模型的表面來放置點。至少需要兩個點（或頂點）才能建立一條路徑。

![GIF顯示路徑工具的選擇與點的建立過程](../../assets/path_create_points.gif)

路徑工具有多種模式，這些模式可能與應用程式中其他可用的繪圖工具相似：

* 沿路徑作畫：沿著定義好的路徑畫一筆規則的筆觸。
* [帶狀路徑](ribbon-tool.md)：沿路徑繪製重複或拉伸的圖像。
* [填滿路徑](filled-path.md)：用均勻顏色填滿路徑內部。
* 沿路徑擦除：畫一條筆劃，沿著定義路徑抹除或移除資訊。
* 沿路徑模糊：畫一條筆劃，沿著定義路徑模糊或模糊資訊。

![工具列截圖，顯示不同路徑工具模式](../../assets/PathTools.png)

例如，以下是路徑工具 **在污漬** 模式下影響其他繪畫資訊：

![GIF顯示路徑工具的模糊模式](../../assets/v90_path_smudge.gif)

>[!NOTE]
>
> **路徑工具**&#x200B;只能在幾何體的表面上使用 3D 空間。目前不支援在 UV 空間或螢幕空間投影中建立路徑。

### 編輯路徑

路徑點（或頂點）會自動附著在網格表面。 它們可以隨時移動和調整。 你可以點擊線上任意位置，為現有路徑新增頂點。

* 按下 **Esc** 或 **Enter** 會退出路徑版。
* 退出後，點擊網格的空白表面即可開始新路徑。
* 滑鼠移鼠並點擊現有路徑即可選擇該路徑，允許繼續或編輯該路徑。 路徑也可以透過路徑&#x200B;**面板重新選擇**（見下文）。

![Gif 顯示新增點的加入及路徑上既有點的移動](../../assets/path_edit_move_points.gif)

有些屬性是針對整體路徑的特有屬性。 這適用於屬性視窗中的&#x200B;**&#x200B;**&#x200B;選項。就像一般筆劃一樣（參見 [繪圖工具文件](paint-brush.md)），可以為路徑定義以下屬性：

* **刷子**
* **阿爾法**
* **材料**

**筆刷**&#x200B;區塊包含僅在路徑工具中提供的額外選項：

| **背景設定** | **描述** |
| --- | --- |
| **投影深度** | 它決定路徑與網格表面的距離，刷子印記才會出現。 若要直接在視窗中看到這些視覺回饋，可以在路徑顯示設定&#x200B;**中**&#x200B;啟用&#x200B;**法線**（見下文）。 |
| **上軸** | 當 **「跟隨路徑** 」偏離時，用來定位刷子印章的軸線。 在某些情境下，讓所有印章沿全局軸/方向排列，而不是沿著路徑排列，會更合理。 例如金屬表面上的鉚釘。 |

路徑上的點（頂點）定義了其他性質，例如壓力。 要編輯特定點，只要點擊它（或使用矩形選取）。 然後用上下文工具列編輯選取的點數值。

![顯示每個頂點壓力的版本 GIF。](../../assets/path_point_pressure_example.gif)

### 控制切線

有時候平滑的路徑並不理想，可能是因為它沒有跟隨最佳的 3D 模型表面，或是不符合特定的外觀。 為了解決這些問題，可以修改給定頂點的切線。 切線是控制路徑彎曲方向的點。

要在平滑或線性/斷裂切線間切換，只需雙擊頂點（或使用情境工具列中的專用按鈕）：

![Gid 示範如何控制路徑上的切線](../../assets/path_break_tangents.gif)

若要更精確地控制切線的方向，請使用情境工具列中的自訂切線按鈕手動覆寫：

![Gid 示範如何控制路徑上的切線](../../assets/path_control_tangents.gif)

如果移動時還沒切換到切線，可以用 **ALT** 鍵盤快捷鍵來斷開切線。

使用 **CTRL** 鍵盤的 Shorcut 同時縮放兩個切線。

>[!NOTE]
>
> 切線控制沿著平面圖定義，並與路徑中給定點的法線對齊。 這表示切線無法在某些方向彎曲。

### 情境工具列

![路徑模式下情境工具列的截圖](../../assets/path_contextual_toolbar_overview.png)

當選擇路徑&#x200B;**工具時**，**情境工具列**&#x200B;提供多種設定，讓你可以控制目前所選的路徑：

<table>
  <tr>
    <th><strong>參數</strong></th>
    <th><strong>說明</strong></th>
  </tr>
  <tr>
    <td><strong>顯示/隱藏視窗介面</strong><br><img src="../../assets/path_contextual_toolbar_showhide.png" alt="路徑工具顯示隱藏圖示"/></td>
    <td>啟用後，路徑和頂點覆蓋層會在視窗中顯示。</td>
  </tr>
  <tr>
    <td><strong>顯示設定</strong><br><img src="../../assets/path_contextual_toolbar_display.png" alt="Paht 顯示設定圖示"/></td>
    <td>控制路徑視覺回饋的外觀：<br><ul><li><strong>把手大小</strong>：控制路徑點的大小。</li><li><strong>路徑寬度</strong>：控制路徑線的厚度。<br></li><li><strong>路徑顏色</strong>：控制路徑線的顏色。<br></li><li><strong>未選取路徑顏色</strong>：控制非啟用路徑的顏色。<br></li><li><strong>法線：</strong>若啟用，請顯示路徑中 eahc 點的投影方向。<br></li><li><strong>切線</strong>：若啟用，顯示路徑控制點的曲線方向。<br></li><li><strong>路徑方向</strong>：若啟用，請在路徑末端顯示一個小箭頭以指示其繪畫方向。 這有助於了解筆劃內印章的方向。</li></ul><br><img src="../../assets/path_contextual_toolbar_display_settings.png" alt="路徑顯示設定面板的截圖"/></td>
  </tr>
  <tr>
    <td><strong>反向路徑方向</strong><br><img src="../../assets/path_contextual_toolbar_direction.png" alt="反向路徑圖示"/></td>
    <td>將當前路徑的方向反轉。 方向定義了在筆劃中繪製郵票的大致方向。 反轉路徑有助於重新調整繪製圖案的方向。</td>
  </tr>
  <tr>
    <td><strong>切換角落 / 平滑</strong><br><img src="../../assets/path_contextual_toolbar_smoothcorner.png" alt="切換光滑角圖示"/></td>
    <td>可以斷開或對齊目前選取頂點的切線，讓它能在平滑曲線或線性曲線間切換。<br><img src="../../assets/path_smooth_corner_demo.png" alt="一張同時有平滑與線性路徑的路徑截圖 "/><br><strong>注意：</strong> 在轉角/平滑行為之間切換，也可以透過雙擊路徑上的某點來完成。</td>
  </tr>
  <tr>
    <td><strong>自訂切線</strong><br><img src="../../assets/path_icon_custom_tangents.png" alt="Paht 工具圖示用於自訂切線"/></td>
    <td>若啟用，允許手動控制路徑上某點的切線。<br><img src="../../assets/paht_cutom_tangents_demo.png" alt="顯示自訂路徑切線的圖片"/></td>
  </tr>
  <tr>
    <td><strong>開啟/關閉路徑</strong><br><img src="../../assets/path_contextual_toolbar_close.png" alt="開閉路徑圖示"/></td>
    <td>開啟或關閉目前的路徑。 要關閉路徑，必須先選擇當前路徑的兩個端點之一。<br><img src="../../assets/v90_path_open_close.gif" alt="GIF顯示路徑先開放後關閉"/></td>
  </tr>
  <tr>
    <td><strong>刪除頂點</strong><br><img src="../../assets/path_contextual_toolbar_delete.png" alt="刪除路徑頂點圖示"/></td>
    <td>移除目前選取的路徑頂點。</td>
  </tr>
  <tr>
    <td><strong>對稱性</strong><br><img src="../../assets/path_contextual_toolbar_symmetry.png" alt="對稱圖示特徵"/></td>
    <td>啟用或關閉目前路徑的對稱性。 更多資訊請參閱 <a href="../symmetry/symmetry.md">對稱性文件</a> 。<br><img src="../../assets/v90_path_symmetry.gif" alt="GIF，顯示對稱繪製路徑"/></td>
  </tr>
  <tr>
    <td><strong>隱藏/忽略排除的幾何</strong><br><img src="../../assets/path_contextual_toolbar_exclude.png" alt="幾何遮罩排除圖示"/></td>
    <td>如果啟用，讓目前路徑穿過隱藏幾何體。 更多資訊請參閱 <a href="../../interface/layer-stack/geometry-mask.md">幾何遮罩文件</a> 。</td>
  </tr>
</table>

### 路徑面板

![路徑面板](../../assets/path_panel_visibility.png)

>[!NOTE]
>
> 當目前的工具不是路徑工具，或選取填充圖層/資料夾時，面板會被隱藏。

視窗內有&#x200B;**&#x200B;**&#x200B;路徑面板，列出目前所選繪畫圖層/效果的所有路徑。它提供了選擇和管理路徑的簡單方式。

透過此面板，可以：

* 雙擊路徑即可 **重新命名** 。
* **選取路徑後按下刪除鍵即可刪除** 。
* **用**&#x200B;專用鍵盤快捷鍵複製/**貼上**/**複製** 路徑。
* **用眼睛圖示顯示** 或 **隱藏** 路徑（控制路徑是否套用到貼圖上）。

為了方便起見，也可以右鍵點擊路徑以開啟上下文選單，該選單提供相同的操作：

![路徑面板右鍵選單](../../assets/path_panel_rightclick_menu_copy_properties.png)

右鍵選單也會開啟將路徑的屬性或位置複製到另一條路徑上的動作。 這讓功能能輕鬆地在不同路徑間共享或同步：

![GIF 展示如何複製並貼上路徑屬性](../../assets/path_copy_paste_properties.gif)![，Gif 示範如何複製並貼上路徑位置](../../assets/path_copy_paste_vertices.gif)

>[!NOTE]
>
> 複製貼上屬性只有在路徑基於相同繪製工具時才有效。 例如，無法在使用模糊設定的路徑與使用刷子設定的路徑間共享屬性。

## 工具預設

![選取路徑工具時，屬性面板預設區段的截圖](../../assets/path_presets.png){width="400px"}

當選取路徑工具時，屬性面板頂端會有一個預設區段。 從這裡你可以快速存取各種路徑工具的預設。

### 最愛路徑預設

預設區的「最愛」選項只會保留你收藏的預設，這樣可以更快存取。 要開始新增收藏，請選擇收藏，然後選擇「在資產中顯示相容預設」，即可查看所有可用路徑預設的完整清單。

要收藏預設，請在資產面板或屬性面板的預設區塊中右鍵點擊該預設，然後選擇「新增到收藏夾」。

你也可以從收藏清單中移除預設。 右鍵點擊「收藏」預設，然後選擇「從收藏夾移除」。

![選取路徑工具時，屬性面板預設區段的截圖。 已選擇「收藏」選項，並勾選「在資產中顯示相容預設」按鈕。](../../assets/ShowCompatiblePresets.png){width="400px"}

### 建立路徑預設

像其他工具一樣，可以建立預設來快速還原筆刷設定/設定。 操作方法是在屬性&#x200B;**視窗中右鍵點擊**，選擇&#x200B;**建立工具預設。** 這個新建立的預設會在資產&#x200B;**視窗中選擇**&#x200B;時自動切換到路徑工具。