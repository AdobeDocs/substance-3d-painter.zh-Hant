---
breadcrumb-title: ''
description: 檢視 Substance 3D Painter 版本的所有變更與更新，以追蹤功能隨時間的演進與改進。
title: ZBrush 至 Painter 橋
user-guide-description: ''
user-guide-title: ''
source-git-commit: c50b48e520277293b9ddef466baf8e27db4891ab
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 0%

---


# ZBrush 至 Painter 橋

從 ZBrush 2026.2.0（Maxon One 2026 年 4 月更新）及 Substance 3D Painter 12.0.2（Steam 與 CC 版本）開始，玩家可以透過最新版本 ZBrush 自動安裝的外掛，直接從 ZBrush 傳送模型到 Painter。

![一張宣傳圖片，展示一個資產在 Zbrush 和 Painter 中被同一資產疊加渲染。](../../assets/zbrush_promotional.png)

有了 Substance Bridge 外掛，就不需要經歷繁瑣的匯出低多邊形和高多邊形檔案、匯入 Painter 以及設定和執行烘焙的繁瑣過程。

要開始使用 Zbrush 轉 Painter 橋接器：

1. 請確保你至少安裝了 ZBrush 2026.2.0 版本。
1. 在 Painter 裡面啟用外掛，確保 **Python > zbrush_painter_plugin** 有被勾選。
1. 從 ZBrush 中，**Send to Painter** 功能可在 Texture > Substance Bridge 中取得&#x200B;**&#x200B;**

![ZBrush 中 Substance Bridge 插件的圖片](../../assets/zbrush_painterSendTo.png)

## 配置

你可以在 Painter 中設定以下自動建立專案的設定：

| 背景設定 | 說明 |
| --- | --- |
| 送給畫家 | 將模型傳送到 Substance 3D Painter，並套用目前設定。 每次點擊都會從零開始創建一個新的 Substance 專案。 |
| **子工具** | |
| 全部 | 不管可見性如何，都會發送所有子工具。 不管眼球是開還是關，所有東西都會被傳送。 |
| 可見 | 只傳送在子工具清單中開啟眼睛圖示的子工具。 |
| 現役 | 只傳送目前選擇的子工具 |
| 發送 PolyPaint | 將 PolyPaint 轉換成貼圖，並在 Substance 中作為填充層套用，這樣你可以在上面繪製並與它混合。 |
| 平滑法線 | 在匯出時平滑切線法線，讓多面面的網格在 Substance 中看起來很平滑，符合遊戲引擎的渲染方式。 關閉後可以看到幾何體的實際切割。 |
| 自動烘焙地圖 | 模型抵達後會自動執行 Substance 的烘焙演算法，從高低網格比較中產生法線貼圖、環境遮蔽、曲率及其他細節貼圖。 |
| 強制紫外線自動展開 | 觸發 Substance 對每個收到的 SubTool 進行 UV 展開演算法。 如果你的模型已經有不錯的 UV，請不要，因為這樣會覆蓋它們。 |
| 分區層級 | 控制傳送的細分等級。 Current 只會傳送顯示的關卡。 低與高會同時傳送烘焙的最低和最高層級，是大多數工作流程的推薦選項。 |
| 材質集 | 控制 Substance 中 UV 空間的劃分：每個子工具（每個子工具一個材質集）或每個多邊形組（每個子工具內的多形組一個材質集合）。 |

當 Painter 收到模型時，如果啟用了自動烘焙，烘焙就會啟動。 模型中最低細分是匯入為低多邊形網格的網格，而最高的子分割則用作高多邊形來烘焙細節。 ZBrush 能處理比 Painter 更多的多邊形，所以要確保低多邊形網格有最佳的工作大小（這會依機器而定，但低於 100 萬是最佳）。

Painter 中的貼圖集代表材質分配。 一個貼圖集等於一個 UV 空間。

* 每個子工具為每個子工具建立一個貼圖集（所有子工具零件共用相同的 UV 空間），這是較簡單的選擇。
* 每個多邊形群會在每個子工具內為多邊形群建立一個貼圖集，讓你對材質分配有更細緻的控制。

>[!NOTE]
>
>在 Steam 版 Painter 中，Painter 必須開放才能接收 ZBrush 模式。


## 其他資源

[觀看此影片](https://www.youtube.com/watch?v=fLkkwV4BzrU)以了解橋樑的運作，或取得 [&#128279;](https://help.maxon.net/zbr/en-us/Default.htm#html/reference-guide/texture/substance-bridge/substance-bridge.html?Highlight=painter) ZBrush 文件以獲得更多資訊。
