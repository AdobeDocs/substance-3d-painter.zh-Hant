---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/release-notes/old-versions/version-2-2.html"
breadcrumb-title: ''
description: 請參閱 Substance 3D Painter 2.2 版本的發行說明，了解新功能、改進與錯誤修正。
helpx_creative_field: ""
helpx_description: Painter > Release notes > Old versions > Version 2.2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 版本 2.2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---


# 版本 2.2

**Substance Painter 2.2** 新增了一個工作流程，稱為動態材質分層。

發行日期： *2016年7月21日*

## 主要特色

### 新的動態材質分層工作流程

![](../../assets/dynamic-material-blending-materials-preview.jpg)

在這個新版本中，我們新增了一個&#x200B;**稱為**&#x200B;材質分層的新&#x200B;**工作流程**。傳統的貼圖工作流程依賴於以高解析度製作貼圖&#x200B;**來**&#x200B;保留細節&#x200B;**，但這**&#x200B;對使用情境來說並不方便&#x200B;**。**&#x200B;更有趣的做法是 **製作小型耕作材料** ，並在 **著色器**&#x200B;中重複進行。 它能保留一定的品質，並能&#x200B;**用這個著色器**&#x200B;非常接近&#x200B;**物件放大而不損失細節**。唯一的問題是，過去要預覽最終結果，必須進入顯示最終著色器的遊戲引擎或渲染器。 但現在已經不一樣了，因為在這個新版本中，Substance Painter 裡可以用類似的著色器，讓你能 **同時視覺化最終結果並進行繪畫**。

新增了一個&#x200B;**名為「** FireHydrant **」的範例專案**，以展示新的工作流程。

![](../../assets/layer-stacks.png)

這個新工作流程開啟了兩種工作方式：

* 材質是在著色器中定義的，你只能用遮罩來混合它們
* 材質和遮罩可以一起塗裝

無論如何，每次都可以定義新的圖層堆疊，這在製作遮罩和材質時會帶來更多自由度。 這樣管理圖層會簡單許多，每個堆疊都可以有自己專屬的通道，可以在最終著色器中混合。\
我們也有專為 Unity 5 和 Unreal Engine 4 提供的特別著色器，可在分享平台取得：

* [Unity 5](https://share.allegorithmic.com/libraries/2126)
* [虛幻引擎4](https://share.allegorithmic.com/libraries/2125)

更多細節請參閱文件中專門的頁面： [動態材質分層](../../features/dynamic-material-layering.md)

### 新的迷你架子搜尋欄位

![](../../assets/mini-shelf-search.gif)

我們改進 **了應用程式中出現在不同位置的迷你書架** ，並設有專門的搜尋欄位。 這項改進讓尋找資源變得更加方便且愉快。 自訂搜尋會在應用程式當前的會話中被保留。 例如，如果你經常使用垃圾搖滾的聲音，使用這個關鍵字就會造成

## 教學

我們最新的影片教學涵蓋了新功能：

## 發行說明

### 2.2.0

（2016年7月21日發行）

**新增：**

* [書架]改進搜尋系統與查詢
* [書架]新增迷你書架搜尋欄
* [著色器]允許定義滑桿的階躍精度
* [著色器]新增復原/重做按鈕用於著色器參數
* [著色器]重新載入著色器不應該重置其參數
* [MatLayering]新增對動態材質分層與子堆疊的支援
* [MatLayering]允許匯入 json 檔案以設定著色器設定
* [MatLayering]解鎖貼圖取樣器限制（切換為無綁定貼圖）
* [腳本]允許設定烘焙者設定並啟動計算
* [內容]除了識別碼外，輸入/輸出連接也使用「使用」
* [工具]允許在投影工具的視窗中選擇預覽通道

**已修正：**

* 如果藥物放在錯誤資料夾裡，啟動時會當機
* 當機報告有時因為日誌檔案錯誤而無法運作
* [Iray]當Iray暫停時，後期效果不會刷新
* [Iray]自動對焦快捷鍵不再有效了
* [Iray]光圈滑桿行為會根據資產大小改變
* [圖層]如果所有素材通道都被關閉，預設不會啟用
* [著色器]如果「param auto」錯誤，則不會列印錯誤

**已知問題：**

* [Mac]貼圖取樣限制鎖定在 16（GPU 驅動程式問題）
