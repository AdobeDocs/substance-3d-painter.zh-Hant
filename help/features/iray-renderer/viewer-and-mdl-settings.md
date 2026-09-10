---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/features/iray-renderer/viewer-and-mdl-settings.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中設定 Iray 渲染器的檢視器和 MDL 設定，以自訂材質渲染。
helpx_creative_field: ""
helpx_description: Painter > Features > Iray Renderer > Viewer and MDL Settings
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 檢視器與 MDL 設定
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 0%

---


# 檢視器與 MDL 設定

![](../../assets/display-settings-iray.png){width="400px"}

## 環境

與一般視窗相同，Iray 使用的環境貼圖將控制光照。\
環境貼圖可透過點擊按鈕或拖放 HDR 材質來更改。

* **環境曝光**  ：控制 HDR 環境地圖的曝光層級。
* **環境旋轉**  ：用來移動環境貼圖並旋轉場景中的光照。

>[!NOTE]
>
> Iray 是基於物理的渲染器，環境貼圖會大幅定義場景的光影和外觀。

## 圓頂

圓頂是背景中環境地圖將投影的形狀。\
有三種圓頂可供選擇，依場景不同而定：

![](../../assets/dome-type.png)

* **無限球**  體：環境投影在背景的球體上，模擬地平線，因此始終遠離場景
* **球面**  ：環境投影在一個可縮放的正球體上
* **帶地面**  的球體：與前一個形狀類似，這個形狀也有控制點可以將球體底部壓平，模擬地板。

>[!NOTE]
>
> 帶地面的球體可以控制地板的大小/半徑，但半徑太大會讓環境產生扭曲。\
>  根據所選的類型，光線可能會受到影響。

還有其他設定可供選擇：

| *背景設定* | *描述* |
| --- | --- |
| **半徑** | 球體的大小（如果不是無限大） |
| **貼圖尺度** | 球&#x200B;**體的貼圖會有多少拉伸**，尤其是地面屬性。 |
| **透明色** | 若啟用，請將環境貼圖的背景影像替換為統一顏色。 這會影響光線。 |

### 地面設定

地面設定允許指定樓層的位置。\
預設值設定為固定場景包圍框底部。

| ***背景設定*** | ***描述*** |
| --- | --- |
| **X、Y、Z 值** | 定義地板在三個軸上的位置。   0,0,0 的值對應場景邊界框的中間位置。 |
| **反射率** | 定義地面反射的強度與顏色。   白色亮度值表示地面是100%反光，黑色則表示完全不反光。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/reflectivity-optim.gif"/></div> |
| **光澤** | 定義反射的光澤程度（或粗糙度）。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r3-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/glossiness-optim.gif"/></div> |
| **陰影強度** | 此參數定義光照計算後陰影的最終不透明度。 |
| **從下方可見** | 定義地面是否從下方可見。 如果被檢查，代表地面會遮蔽上方的任何元素。 |

## MDL 與著色器參數

Iray 使用 MDL 來定義用於渲染物件的材質。 欲了解更多資訊，請參閱  [官方 Nvidia 格式頁面](http://www.nvidia.com/object/material-definition-language.html)  。

在 Substance 3D Painter 中，預設情況下，MDL 會與 GLSL 著色器相關聯，讓玩家能在一般視埠與 Iray 之間切換，無需設定任何設定。\
MDL 的參數會顯示在檢視器設定的底部。 以下是預設 MDL（與 PBR 金屬/粗糙度著色器相容）的參數。

>[!NOTE]
>
> 要載入自訂 MDL，需要自訂的 glsl 著色器。\
>  在著色器中，可以加入一些 metadat 來指定 mdl 路徑：
> 
> &#x200B;- 宣告 iray mdl 材質以配合此著色器使用。 ： metadata { //： “mdl”：“mdl：:alg::materials::p hysically\_metallic\_roughness：:p hysically\_metallic\_roughness” //： }
> 
> * **MDL**  ：定義用於著色器的 Iray MDL 材質。 路徑語法如下：  *mdl：:folder1::folder2:：mdl\_filename：：material\_name*  其中  *folder1：:folder2:：mdl\_filename*  是你架子  *mdl*  資料夾內通往 mdl 檔案的路徑，而  *：：material\_name*  是該 mdl 檔案中宣告的材質名稱。 （例如：「MDL」：「MDL：:alg::materials::p hysically\_metallic\_roughness：:p hysically\_metallic\_roughness」）

>[!NOTE]
>
> 專案中的每個物料實例都會設定一個 MDL。 因此，為了將材質屬性分開在貼圖集之間，設定新的材質實例來完整配置 MDL。

![](../../assets/mdl.png)

Substance 3D Painter 的預設 MDL 支援以下特性：

| *背景設定* | *描述* |
| --- | --- |
| **發射強度** | 發射通道的乘法器。 高值會開始發光。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r1-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/emissive-optim.gif"/></div> |
| **折射** | 控制折射量。 |
| **IOR** | 定義材料的折射率。   註：空氣 = 1.0，水 = 1.2，玻璃 = 1.5。 |
| **散射** | 控制光線在表面散射的量。 |
| **吸收** | 控制表面吸收多少光。 |
| **吸收色** | 模擬光線穿過表面時顏色的變化。 |
