---
breadcrumb-title: ""
description: 存取 Substance 3D Painter 的 All Rendering States Params 著色器 API 參考，以控制渲染狀態參數。
title: 所有渲染狀態參數 - 著色器 API
user-guide-description: ""
user-guide-title: ""
source-git-commit: 6b6d52207ca1d043aaa1b2b14145b6b49d4c1942
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%
---

# 所有渲染狀態參數 - 著色器 API

## 渲染狀態範例

## 背面剔除

剔除背部面：

```
//: state cull_face on
```


畫正面與背面：

```
//: state cull_face off
```


## 混合

沒有混合、完全不透明的物件：

```
//: state blend none
```


標準混合模式，用於前後拉弓順序：

```
//: state blend over
```


標準混合模式，用於前後拔槍順序。 假設顏色已先乘以α：

```
//: state blend over_premult
```


加法混合模式：

```
//: state blend add
```


乘法混合模式：

```
//: state blend multiply
```


## 著色器取樣區域

預設情況下，文件通道會使用未轉換的材質座標取樣，以便在繪製過程中進行渲染優化。

若出現偽影，則將非局域&#x200B;*狀態設*&#x200B;為 *。*

```
//: state nonlocal on 

 
```
