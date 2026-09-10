---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/features/iray-renderer/iray-settings.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中設定 Iray 渲染器設定，以控制渲染品質與效能。
helpx_creative_field: ""
helpx_description: Painter > Features > Iray Renderer > Iray Settings
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Iray 設定
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 0%

---


# Iray 設定

![](../../assets/iray-settings.png)

Iray 設定控制 IRay 視窗的渲染、運行時間和品質。

## 伊雷資訊

視窗頂端顯示伊雷的狀態及其他資訊。

| *背景設定* | *描述* |
| --- | --- |
| **現況** | 狀態顯示 Iray 的工作狀況：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>渲染</strong> （Iray 正在計算影像）</li><li data-preserve-html="true"><strong>暫停</strong> （Iray 計算停止但尚未完成）</li><li data-preserve-html="true"><strong>完成</strong> （Iray 計算完成，或達到設定值）</li></ul> |
| **解決方法** | Iray 影像的解析度（預設依視窗大小而定）。 |
| **場景規模** | 場景/3D 網格的包圍盒大小。 沒有單位，但假設單位是公分。 |
| **迭代** | Iray 執行的計算次數超過設定中定義的最大值。 |
| **渲染時間** | 渲染時間在設定中定義的最大範圍內經過。 |

>[!NOTE]
>
> 迭代次數決定最終渲染品質：迭代次數越多 = 品質越好。\
> 然而，迭代可能需要一些時間，因此可以定義最大時間。 迭代以取樣數定義。

## 設定

一旦設定被修改，Iray 就會開始計算渲染。\
你可以用專用按鈕暫停 Iray 以避免此行為：

![](../../assets/pause-2.png)

| *背景設定* | *描述* |
| --- | --- |
| **最小樣本** | 像素所執行的最小取樣數 |
| **麥克斯·桑普爾** | 像素執行的最大取樣量 |
| **最大時間** | Iray 完成計算的最大時間。  右側下拉選單可設定單位（秒、分鐘或小時）。 |
| **啟用苛性取樣器** | 此選項可計算更進階的光反射（焦散）。 |
| **啟用螢火蟲過濾器** | 這個選項可以消除偶爾會出現的孤立且非常亮的像素。 |
| **Override 視窗解析** | 此設定允許自訂渲染大小，而非使用目前的視窗大小。 **下方的寬度**&#x200B;與&#x200B;**高度**&#x200B;設定允許以像素數量來定義。 |
| **儲存渲染** | 將目前渲染（即使尚未完成）匯出成檔案的動作。 |
| **分享** | 允許分享/匯出目前渲染圖到 [ArtStation](https://www.artstation.com/)。 |
