---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/interface/shader-settings/updating-a-shader.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中更新自訂著色器，以套用著色器變更並重新載入著色器檔案。
helpx_creative_field: ""
helpx_description: Painter > Interface > Shader settings > Updating a shader
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 更新著色器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---


# 更新著色器

有時需要更新專案所使用的著色器，以修正問題或利用最新功能。 本頁說明了如何做到這一點。

以下是兩個逐步更新專案著色器的方法：

* **透過著色器視窗更新著色器**
* **透過 Resource Updater 外掛更新著色器**

如果專案使用  **自訂著色器**  （Substance 3D Painter 預設不附帶），請參考  [自訂著色器](https://substance3d.adobe.com/display/DRAFTPAINTER/Shader+API)  頁面，取得更新指南。

## 透過著色器視窗更新著色器

### 1 - 開啟著色器設定視窗

**著色器設定**&#x200B;視窗預設在 Dock 工具列右側。

![](../../assets/shader-settings-window.png)

### 2 - 點擊著色器按鈕並選擇更新後的著色器

點擊著色器按鈕（在復原/重做按鈕下方），找到與已使用的著色器相符的著色器。

![](../../assets/shader-mini-shelf.png)

### 3 - 著色器更新

一旦載入新著色器，應該會移除「過時&#x200B;**」的標示**，3D 模型會正常出現在視窗中。

![](../../assets/updated-shader.png)

## 透過 Resource Updater 外掛更新著色器

### 1 - 開啟資源更新器

往介面左側走到  **插件工具列**  ，點選  **資源更新**  器圖示。

![](../../assets/resource-icon.png)

### 2 - 切換到著色器分頁

在新出現的視窗中，點擊「著色器」標籤即可顯示目前專案中的著色器。

![](../../assets/shader-tab.png)

### 3 - 找到著色器並更新它

在 Shader 標籤中，應該會顯示目前專案所有使用者的 Shader 資源清單。 **過時的**  著色器會顯示為  **紅色背景**  。 點擊資源旁的「更新」按鈕來更新。

![](../../assets/update-shader-click.gif)
