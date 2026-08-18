---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/technical-issues/startup-issues/application-failed-to-start-because-of-qt.html"
breadcrumb-title: ''
description: 學習如何修復因 Qt 框架問題導致的 Substance 3D Painter 啟動失敗，以正確啟動應用程式。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Startup Issues > Application failed to start because of Qt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 申請因 Qt 問題未能啟動
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---


# 申請因 Qt 問題未能啟動

啟動應用程式時可能會跳出以下錯誤訊息：

>> 

此應用程式無法啟動，因為無法初始化任何 Qt 平台外掛。 重新安裝應用程式可能會解決這個問題。

可用的平台外掛有：最小型、離線、webgl、windows。

此錯誤可能因另一個軟體定義環境變數與應用程式衝突而產生。

在啟動應用程式前，請務必從目前環境中移除以下變數：

```
QT_PLUGIN_PATH 

QML2_IMPORT_PATH
```


>[!NOTE]
>
> 這些變數也可以從 Python 上下文繼承，例如 **pyinstaller**。 務必將它們從應用程式啟動的上下文中移除。
