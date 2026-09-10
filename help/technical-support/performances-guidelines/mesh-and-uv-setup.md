---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/performances-guidelines/mesh-and-uv-setup.html"
breadcrumb-title: ''
description: 學習 Substance 3D Painter 中網格與 UV 設定的最佳實務，以優化效能與貼圖品質。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Performances guidelines > Mesh and UV setup
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 網格與 UV 設定
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 0%

---


# 網格與 UV 設定

花幾分鐘準備 Painter 的網格，可以讓貼圖過程更快更輕鬆。

+++高多邊形數模型
Painter 沒有專門能處理的多邊形數量基準，因為這很大程度上取決於機器規格、貼圖集分配和圖層堆疊屬性，但如果考慮到圖層堆疊優化，少於 1000 萬多邊形應該也能應付。

+++

+++低多邊形數量模型
有過低多邊形的情況。 這是因為材質引擎會利用多邊形來判斷網格的哪一部分該被渲染，以計算筆觸。 多邊形數非常低的網格即使只用極小的筆觸，也能完全重新渲染，這會讓 GPU 過度負擔。

例如，如果要貼圖一個四邊形平面，最好將網格細分，尤其是在手繪時用大量筆觸，因為資訊分散在更多頂點上。

+++

+++將紋理分割到多個紋理集
最好將較大且材質分配較複雜的網格拆分成多個貼圖集。 貼圖集允許你為每個貼圖集指派不同的設定，例如解析度和著色器屬性。 例如，如果網格只有部分使用半透明或 SSS，最好為該部分指派另一個貼圖集和不同的著色器實例。 這樣一來，這些較複雜的特性就不必在未被使用的地方計算。

+++

+++讓紫外線島靠近
盡量讓三維空間中相鄰的 UV 島嶼保持彼此靠近。 這同時適用於 UDIM 佈局和經典的 UV 空間佈局。 如果它們有相同的繪畫筆觸或貼圖，當它們聚集在 UV 空間的同一區域時，會比在相反端更容易計算。

材質引擎透過將材質分割成較小的區塊來加速計算。 這表示每次筆劃只會更新需要修改的區塊，而不是每次筆觸都更新整個貼圖。 透過讓鄰近的 UV 島嶼彼此靠近，可以減少單一筆劃影響的區塊數量。

+++

+++避免物品太多
當匯入子物件少於 8000 個的網格時，效能應該會保持舒適。 超過這個限制會影響視窗和繪製效能。 若達到此限制，我們建議將物件合併以降低渲染負擔。

+++
