---
helpx_url: 'https://helpx.adobe.com/substance-3d-painter/interface/viewport.html'
description: 學習如何在 Substance 3D Painter 中使用視窗，在上色過程中視覺化你的 3D 模型與材質。
helpx_description: Painter > Interface > Viewport
title: 視框
source-git-commit: 7b5f6e6c9623cb51253b6e49c8dbcbb22856418c
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 1%

---


# 視框

![](../../assets/viewports-progress.jpg){width="600px"}

視窗是顯示 3D 網格及其材質的地方。 這也是可以在 3D 網格表面上繪製的地方。

## 概觀

觀景窗分為四個部分：

* **情境工具列**：這個工具列位於視窗頂端，根據當前情境提供各種屬性的快捷方式（例如繪製時的筆刷參數）。
* **3D 視圖**：此視角顯示由攝影機定義的特定角度的 3D 網格。
* **2D 視圖**：此視圖顯示目前選取 [的貼圖集](../texture-set/texture-set-list.md) 3D 網格的 UV 展開。
* **進度條**：當計算進行中（例如引擎產生材質時），這個位於視窗底部的灰綠色條會顯示。

更多詳情請參閱專屬頁面：

* [2D 視角](2d-view.md)
* [3D 檢視](3d-view.md)
* [攝影機管理](camera-management.md)

3D 與 2D 視圖可透過 [顯示設定](../../interface/display-settings/display-settings.md)調整以顯示額外或不同的資訊。

## 視窗導航控制

在 2D 和 3D 視角中，移動視窗的控制方式相似。

<table>
  <tr>
    <th>機芯類型</th>
    <th>捷徑</th>
    <th>說明</th>
  </tr>
  <tr>
    <td>軌道/旋轉<br></td>
    <td><strong>Alt + 左鍵點擊</strong></td>
    <td><ul><li>3D 視角：將相機繞著游標位置旋轉。</li><li>2D 視圖：將 UV 空間繞著游標位置旋轉。</li></ul></td>
  </tr>
  <tr>
    <td>平移</td>
    <td><strong>Alt + 中鍵點擊</strong></td>
    <td>將攝影機往上、下、左或右移動。</td>
  </tr>
  <tr>
    <td>變焦/推車</td>
    <td><strong>Alt + 右鍵</strong></td>
    <td>縮放到或更靠近或遠離網格/UV。</td>
  </tr>
</table>

>[!NOTE]
> 在 2D 和 3D 視角中，你可以用 Alt + Shift + 左鍵&#x200B;**點擊繞圈/旋轉**&#x200B;時，直接吸附成正交角度。

## 改變版面配置

預設的配置是 3D 視圖在左邊，2D 視圖在右邊。 情境工具列&#x200B;**中有**&#x200B;幾個參數可用來更改版面配置：

<table>
  <tr>
    <th><em>背景設定</em></th>
    <th><em>說明</em></th>
  </tr>
  <tr>
    <td><strong>視窗模式</strong><br>！[&#128279;](../../資產/viewport-viewmode.png)</td>
    <td>這些設定控制視窗的佈局：<br><ul><li><strong>3D/2D</strong> （預設）：在視窗中同時顯示 3D 與 2D 視圖</li><li><strong>僅限</strong> 3D：最大化 3D 視圖並隱藏 2D 視圖。</li><li><strong>僅限</strong> 2D：最大化 2D 視圖並隱藏 3D 視圖。</li><li><strong>交換 3D/2D</strong>：交換視圖顯示的順序。 如果 3D 視角在左邊，選擇這個動作後就會在右邊。</li></ul></td>
  </tr>
  <tr>
    <td><strong>視角模式</strong><br>！[&#128279;](../../資產/viewport-camera-projection.png)</td>
    <td>以下設定控制 3D 網格在 3D 視圖中的呈現方式：<br><ul><li><strong>透視視角</strong> （預設）：顯示3D網格，呈現人眼或相機所見的樣貌。</li><li><strong>正交視圖</strong>：顯示3D網格，因為每個方向測量的長度相同。</li></ul></td>
  </tr>
  <tr>
    <td><strong>攝影機旋轉模式</strong><br>！[&#128279;](../../資產/viewport-camera-axis.png)</td>
    <td>這些設定控制視窗攝影機可以旋轉多少軸。<br><ul><li><strong>自由旋轉</strong>：相機在 X、Y 和 Z 軸上旋轉。</li><li><strong>受限旋轉</strong> （預設）：鏡頭只在X軸和Y軸旋轉（無滾轉）。</li></ul></td>
  </tr>
  <tr>
    <td><strong>渲染模式</strong><br>！[&#128279;](../../資產/viewport-rendering.png)</td>
    <td>切換到 <a href="../../features/iray-renderer/iray-renderer.md">渲染模式</a>。</td>
  </tr>
</table>
