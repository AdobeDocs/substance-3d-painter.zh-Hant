---
title: 鏡頭光暈
description: ''
helpx_description: "Substance 3D Painter"
helpx_url: "https://helpx.adobe.com/substance-3d-painter/features/post-processing/lens-flare.html"
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---


# 鏡頭光暈

![](../../assets/v12_post_flare.jpg)

模擬強光源與相機鏡頭元件互動時產生的光學偽影，產生光暈、條紋及幽靈反射。

| <b>參數</b> | <b>描述</b> |
| --- | --- |
| <b>解決方法</b> | 設定鏡頭光暈效果的內部渲染解析度。 較高的數值會產生更銳利的條紋，但可能會影響性能。 |
| <b>相機</b> | 選擇用於模擬耀斑的攝影機模型。 可能的數值包括：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>全景鏡頭</b> （較短焦距）</li> <li data-preserve-html="true"><b>長焦鏡頭</b> （較長焦距）。</li> </ul> |
| <b>金額</b> | 控制耀斑效應的整體強度。 數值可以超過1.0來增加強度。 |
| <b>門檻</b> | 決定產生耀斑所需的影像最低亮度。 較低的數值會產生更多區域產生耀斑，而較高的數值則限制效應僅限於非常明亮的光源。 |
| <b>光圈刻度</b> | 可縮放用於光斑計算的孔徑形狀大小，影響光斑元件的整體大小。 |
| <b>被毛厚度</b> | 模擬鏡頭元件上的防反光塗層。 塗層厚度會影響光線散射，進而改變喇叭的顏色。 |
| <b>外套 IOR</b> | 模擬鏡片的折射率：光線如何穿透其厚度。 較低的數值產生更濃縮的幽靈。 |
| <b>遮蔽量表</b> | 設定受影響中心區域的大小。 |
| <b>遮擋平滑度</b> | 控制鏡頭光暈逐漸消退的程度。 較高的數值會產生較柔和的過渡。 |
| <b>獨特的鬼魂</b> | 定義了喇叭形狀的多樣性。 較高的數值可能會顯著影響效能。 |
| <b>幽靈位置尺度</b> | 控制閃光幽靈的擴散與大小。 |
| <b>光圈紋理</b> | 定義用於產生光暈圖案的透鏡光圈形狀。 材質控制繞射和幽靈形狀。 |
