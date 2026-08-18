---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/interface/shader-settings.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中設定著色器設定，以自訂材質渲染與視覺外觀。
helpx_creative_field: ""
helpx_description: Painter > Interface > Shader settings
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 著色器設定
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---


# 著色器設定

![](../../assets/shader-settings.png)

**著色器設定**&#x200B;視窗可控制著色器（及 Iray mdl）參數與幾何位移參數。

著色器是一個函式，用來定義物件在與視窗中光影互動時應呈現的樣貌。 在此應用程式中，著色器用來讀取紋理集通道並在視窗中渲染 3D 網格。

## 還原堆疊與著色器檔案

![](../../assets/shader-undo.png)

著色器設定視窗的這個區塊控制著色器操作時的主要參數。\
著色器的復原/重做堆疊是獨立於主  [歷史](https://substance3d.adobe.com/display/DRAFTPAINTER/History)  的，避免在塗裝時產生衝突。

如果著色器檔案被標記為「過時」，建議在可能的情況下更新它。 參見：  [更新著色器](https://substance3d.adobe.com/display/DRAFTPAINTER/Updating+a+Shader)

| *背景設定* | *描述* |
| --- | --- |
| **還原** | 還原/取消著色器檔案的變更或任何著色器參數修改 |
| **重來** | 重新套用已透過撤銷的變更。 |
| **著色器檔案** | 顯示目前使用的著色器檔案按鈕。 點擊按鈕即可開啟迷你書架並選擇不同的著色器。 |
| **實例名稱** | 著色器實例的名稱。 |
| **還原預設值** | 將所有著色器參數還原到預設值（如著色器檔案中所示）。 |

### 著色器實例

著色器實例是基於原始著色器檔案但有自訂參數的著色器。 著色器實例可以在材質集間共享，而貼圖集也可以擁有獨特的著色器實例。

**舉例來說：**  一個專案可以使用基礎著色器，而一個貼圖集則使用自訂著色器來支援不透明度。

要建立和管理著色器實例，請參閱 [貼圖集清單](../texture-set/texture-set-list.md) 視窗。

## 著色器參數

![](../../assets/shader-parameters-1.png)

著色器參數依賴於目前載入的著色器檔案。

## 位移與鑲嵌

![](../../assets/disp-parameters.png)

位移與鑲嵌是兩種可用來修改物體形狀以增加細節的功能。

* **位移**：根據輸入通道推移或偏移幾何形狀。
* **鑲嵌**：將幾何細分以使其密實。 密度越高，多邊形間距越短，細節越細緻。

架子中有一個名為「**高度到法線**」的濾波器可用，可用來取得最終法線貼圖（以防原生轉換不夠強）。

### 置換

以下是排氣設定：

| *背景設定* | *描述* |
| --- | --- |
| <b> 來源頻道 </b> | 網格變形所基於的通道。 預設是高度，但也可以設定為位移。 |
| <b>比例單位</b> | 選擇位移刻度的定義方式：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>正規化： </b>位移尺度是相對於網格包圍盒大小的。</li> <li data-preserve-html="true"><b>場景： </b>位移比例是相對於匯入場景檔案的單位。</li> <li data-preserve-html="true"><b>物理尺寸（公分）：</b>位移尺度以公分為單位，根據物體的物理大小來衡量。</li> </ul> |
| <b> 比例</b> | 根據所選縮放單元，控制專案中對網格施加的變形量。 |

>[!NOTE]
>
> 場景<b></b>與<b>實體尺寸（cm）</b>比例單位設定都要求進口模型已準備好進行實體尺寸測量。如果匯入檔案中單位設定不正確，或匯入檔案類型不支援實體大小單位，位移仍可行，但可能無法提供你需求的準確結果。

### 鑲嵌

以下是鑲嵌設定：

| *背景設定* | *描述* |
| --- | --- |
| **細分模式** | 決定如何計算細分的數量。 可用的配置有：<ul data-preserve-html="true"><li data-preserve-html="true"> 制服（預設） </li><li data-preserve-html="true"> 邊長 </li></ul> |
| **分區數量** | （模式統一）從1到32。 高值會產生更多多邊形，這會提供更多細節，但也可能帶來效能問題。 |
| **最大長度** | （模態邊長）1 / 值。 每個多邊形邊都會被分割，直到每個段段大小等於或更短，1/1 是場景的大小。 |
