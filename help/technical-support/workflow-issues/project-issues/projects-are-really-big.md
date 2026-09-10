---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/workflow-issues/project-issues/projects-are-really-big.html"
breadcrumb-title: ''
description: 學習如何縮小 Substance 3D Painter 專案檔案大小，以優化效能與儲存需求。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Workflow Issues > Project Issues > Projects are really big
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 專案真的很大
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 0%

---


# 專案真的很大

Substance 3D Painter 專案可以非常龐大，且佔用大量磁碟空間。 本頁說明原因及如何減輕此問題。

## 專案中儲存了哪些資源？

在貼圖過程中使用的每個資產或資源都會儲存在專案檔案中，包括：

* **Source Mesh**  （不是原始檔案，而是已處理過的）
* **烘焙網格貼圖**
* **材料**  （如物質材料）
* **任何圖層/預設/筆觸都會用到位圖**  或其他資源。

高多邊形網格未包含在本專案中。 它們只是相互連結。

## 為什麼一個專案會儲存這麼多資源？

儲存所有使用的資源，使專案完全自主，能輕鬆在不同電腦間移動而不破壞。 主要缺點是硬碟上可能佔用較大的檔案空間。

決定將所有內容嵌入專案檔案，是因為所有東西都是非破壞性的。 這表示當專案重新開放時，會「重建」自己。 如果架子上缺少一根刷子或材料，專案可能會損壞，無法正確再生。 儲存一份資源副本，確保專案仍能像被保存時一樣還原。

## 有沒有辦法縮小專案規模？

有幾種方法可以縮小專案規模：

### 清理未使用的資源

當專案中使用大量資源時，Substance 3D Painter 會複製它們。 例如，如果你用 alpha 來畫某樣東西。 如果你在 alpha 上色時刪除該圖層，Substance 3D Painter 不會自動移除該資源。

要移除未使用的資源，請使用&#x200B;**檔案選單[&#128279;](https://substance3d.adobe.com/display/DRAFTPAINTER/File+menu)中的清理**&#x200B;操作。然後儲存專案（這會觸發實際移除該資源）。

專案中仍在使用的資源無法移除。 這表示停用貼圖集仍能參考資源，並防止它們被刪除。 為了避免這種情況，請在貼圖集重新指派視窗[&#128279;](../../../interface/texture-set/texture-set-reassignment.md)中移除已停用的貼圖集。

### 降低紋理集解析度

當專案被儲存時，Texture Set 的圖層堆疊最終結果會被儲存在專案中。 這讓專案重新開啟時，可以在視窗中保留預覽，而無需重新計算貼圖集。 不過材質集的解析度越大，預覽快取就會越大。

要減少快取佔用，只要把解析度改成較低的數字，例如512。 由於 Substance 3D Painter 是非破壞性的，這個解析度可以之後調整回來而不會損失畫質。

### 壓縮專案

大量以增量方式儲存專案檔案會讓檔案破碎。 雖然不是嚴重問題，但這可能會在專案檔案中產生空位，進而增加檔案大小。

請使用檔案選單[&#128279;](../../../interface/main-menu/file-menu.md)中的「儲存並壓縮」功能重新儲存專案並移除浪費的空白空間。這個存檔動作會比一般存檔長，但能大幅減少檔案佔用空間。

### 縮小烘焙的網格貼圖大小

一般來說，專案佔用磁碟空間的最大原因，是因為烘焙的網格貼圖本身又多又大。

要縮小網格貼圖大小，有幾件事可以做：

* *使用較低的烘焙解析度。*\
  雖然法線貼圖如果能烘焙成 4K，但位置貼圖通常只是彩色漸層，可能就不適用了。 用兩種不同解析度烘焙兩次，混合不同檔案大小。
* *匯出材質並手動減少它們的佔地面積。*\
  Substance 3D Painter 預設會將所有材質烘焙成 16 位元的 RGBA 影像，這包括灰階烘焙器如環境遮蔽。

  要減少烘焙紋理，請使用以下步驟：
  1. 在 Baker 視窗中關閉「套用擴散」設定
  1. 將「Dilation With」設定為合理的值（例如2048解析度時32像素）
  1. 把所有材質都烘烤成同一解析度
  1. 將帶有匯出預設的「Mesh Maps」烘焙貼圖匯出為 16 位元 PNG，填充設為「No padding（直通）」
  1. 請用照片編輯軟體或 Substance 3D Designer 開啟每張地圖
  1. 降低看起來適合的材質解析度。 記得把環境遮蔽、曲率和厚度從彩色切換成灰階。
  1. 將新的材質版本存為 16 位元 PNG。
  1. 重新匯入材質，並在 Texture Set 中替換到原始烘焙材質上。
  1. 在檔案選單中使用清潔操作移除舊的網格貼圖。
  1. 在檔案選單中使用「儲存與壓縮」動作來壓縮專案檔案。\
     完成所有這些步驟後，專案規模應該會大幅縮減。

網格貼圖至少保持 16 位元材質非常重要。 雖然 8 位元材質的佔用面積較小，但它們會在智慧材質與遮罩產生器中引入雜訊。 我們推薦 PNG 是因為它是無損壓縮格式，代表它仍能壓縮材質而不會產生失真，且支援 16 位元。
