---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/pipeline-and-integration/configuration/environment-variables.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中使用環境變數來設定應用程式行為與管線整合。
helpx_creative_field: ""
helpx_description: Painter > Pipeline and integration > Configuration > Environment variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 環境變數
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 2%

---


# 環境變數

本頁列出可用來覆寫應用程式預設行為的環境變數。

| 變數 | 說明 | 版本 |
| --- | --- | --- |
| **內容\_PAINTER\_LICENSE** | 價值：直接連接到授權檔案本身的路徑。允許 覆蓋授權檔案的預設位置。 舉例來說：如果授權檔案在 **H：/allegorithmic/licenses/substance\_painter.key**，變數資料應該是&#x200B;**「H：/allegorithmic/licenses/substance\_painter.key」。****注意：**  對於 3.x（2017.x）之前的版本，請使用 SUBSTANCE\_PAINTER\_2\_LICENSE。 | <ol data-preserve-html="true"><li data-preserve-html="true">1</li></ol> |
| **阿勒_LICENSE\_IDLE\_DELAY** | 值：7200 指定多使用者配置時釋放授權席位的秒數。 預設是2小時（7200秒）。 | <ol data-preserve-html="true"><li data-preserve-html="true">1</li></ol> |
| **ALG\_PAINTER\_SKIP\_CHECK\_FOR\_UPDATES** | 值 ：0 或 1（1 = 停用更新檢查）允許在應用程式啟動時跳過更新檢查。 關閉「What&#39;s new」面板。 | <ol data-preserve-html="true"><li data-preserve-html="true">2.2</li></ol> |
| **實質_PAINTER\_SVT\_HARDWARE\_ACCELERATION** | 值：0 或 1（1 = 啟用）使用 GPU 上的稀疏功能。 如果 GPU 或作業系統不支援，該設定將被忽略。 關於相容硬體配置，請參閱文件：[稀疏虛擬貼圖](../../features/sparse-virtual-textures.md)此變數覆蓋設定視窗中[](../../interface/settings/settings.md)可用的參數。 | <ol data-preserve-html="true"><li data-preserve-html="true">3</li></ol> |
| **內容\_PAINTER\_TEMP_LOCATION** | 值：直接路徑至資料夾定義 Substance Painter 應該寫入暫存檔案（包括 SVT 快取）的位置。此變數覆蓋設定視窗中[](../../interface/settings/settings.md)可用的參數。 | <ol data-preserve-html="true"><li data-preserve-html="true">3</li></ol> |
| **內容\_PAINTER\_PREVIEWS\_MEMORY\_BUDGET** | 值：500 定義應用程式可用來載入並暫時儲存資產視窗預覽的記憶體（記憶體）量。 當預算達到上限時，舊預覽會被卸載。 這個值只控制資產視窗中預覽的顯示。數值以兆位元組為單位定義。 預設值是 500MB。 | <ol data-preserve-html="true"><li data-preserve-html="true">2</li></ol> |
| **內容\_PAINTER\_PLUGINS\_PATH** | 額外 Python 外掛的位置。 | 6.1 |
| **PYTHONPATH** | 額外的 Python 模組，以配合應用程式的 Python 整合來載入。 更多資訊請參見 [「載入外部 Python 模組](https://helpx.adobe.com/substance-3d/unlisted/documentation/spdoc/loading-external-python-modules-205363420.html)」。 | <ol data-preserve-html="true"><li data-preserve-html="true">1</li></ol> |
| **OCIO** | 路徑指向 **一個 config.ocio** 檔案，用來驅動 [OpenColorIO 的色彩管理](../../features/color-management/color-management.md) 設定。  **注意：**  此環境變數優先於 **PAINTER\_ACE\_CONFIG** 變數。 | <ol data-preserve-html="true"><li data-preserve-html="true">4</li></ol> |
| **畫家\_ACE\_CONFIG** | 一個 json 檔案的路徑，用來驅動 [Adobe ACE 的色彩管理](../../features/color-management/color-management.md) 設定。 | <ol data-preserve-html="true"><li data-preserve-html="true">1</li></ol> |
| **內容\_DISABLE\_SPECIFIC\_FEATURES** | 在應用程式中停用多項功能：<ul data-preserve-html="true"><li data-preserve-html="true">外部資源連結（說明、網頁、範例等）</li><li data-preserve-html="true">關閉更新檢查</li><li data-preserve-html="true">停用使用統計資料的傳送</li><li data-preserve-html="true">關閉匯出至物質分享</li><li data-preserve-html="true">關閉歡迎與新內容面板</li></ul> | <ol data-preserve-html="true"><li data-preserve-html="true">1</li></ol> |
| **ALG\_PAINTER\_DEBUG\_FPS** | 在視窗內顯示該視窗每秒渲染的幀數計數器。 | <ol data-preserve-html="true"><li data-preserve-html="true">1</li></ol> |
| **實質\_PAINTER\_VRAM\_BUDGET** | 指定 Painter 能使用多少 GPU 記憶體。 這定義了以 MB 表示的全球預算。 例如，若要定義 4GB 的限制，請使用值 4000。命令列參數也可用來執行相同動作。 請參見 [命令列](command-lines.md)。 | <ol data-preserve-html="true"><li data-preserve-html="true">2.1</li></ol> |
