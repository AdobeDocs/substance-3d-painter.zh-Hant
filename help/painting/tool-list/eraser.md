---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/painting/tool-list/eraser.html"
breadcrumb-title: ''
description: 使用 Substance 3D Painter 中的橡皮擦工具，精確控制移除 3D 模型中的油漆和材質。
helpx_creative_field: ""
helpx_description: Painter > Painting > Tool list > Eraser
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 橡皮擦
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---


# 橡皮擦

橡皮擦是一種用來抹除或隱藏先前被其他工具塗過的油漆工具。 這個工具一次只影響一層。

橡皮擦與繪圖工具共享相同的參數與行為。 想了解更多關於筆刷、alpha 和模板控制的資訊，請參考 [Paint 工具頁面](paint-brush.md)。

>[!NOTE]
>
> 技術上來說， **橡皮擦其實並不會真正移除資訊**。 它只是把圖層 alpha 設回零，這樣就能抹掉或隱藏之前的繪畫資訊。 這表示：
> 
> * 在重新開啟專案後，使用橡皮擦筆觸前，仍會計算出先前已繪製的筆觸。
> * Substance 濾波器如果忽略 alpha 資訊，就能取得 paint 資訊
> 
> 這也是為什麼有時候比起用橡皮擦，更建議 **刪除一個圖層再重新建立** ，因為這樣能提升效能。

## 材質

在刪除資訊時，可能只影響特定通道。

>[!NOTE]
>
> 與繪圖工具不同，橡皮擦只允許定義受影響的通道。 無法從架子載入資源來影響每個通道。

* 若所有頻道皆啟用，橡皮擦器會移除所有頻道內的資訊：

  ![](../../assets/eraser-all-channels-selection.png)

  ![](../../assets/erase-all-channel-optim.gif){width="325px"}
* 若選擇特定頻道，橡皮擦只會從該頻道移除資訊：

  ![](../../assets/eraser-one-channel-selection.png)

  ![](../../assets/erase-one-channel-optim.gif){width="325px"}
