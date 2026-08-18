---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/technical-support/workflow-issues/project-issues/preserve-brush-strokes-setting-stays-disabled.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中修正「保留筆觸」設定一直被停用，以正確保留筆觸。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Workflow Issues > Project Issues > Preserve brush strokes setting stays disabled
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 保留筆觸設定仍被關閉
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---


# 保留筆觸設定仍被關閉

由於 Substance 3D Painter 1.5 引入的一個不幸錯誤（1.7 部分修正），部分專案遺失了與網格相關的元資料。 因此，這個錯誤使得專案設定[&#128279;](../../../interface/project-configuration.md)視窗中的「保留網格筆劃位置」設定被禁用。

要解決這個問題，需要遵循一些具體步驟：

* 請以 Substance 3D Painter 1.7 或更高等級的版本開啟該問題的專案
* 前往編輯>專案設定
* 選擇並重新匯入你目前專案中使用的原始網格（不是更新版本）
* 驗證後讓 Substance 3D Painter 計算圖層，如果是同一個網格，應該不會有變化
* 再回到編輯>專案設定
* 「保留網格上的筆劃位置」現在應該會重新啟用，讓你能匯入新的網格
