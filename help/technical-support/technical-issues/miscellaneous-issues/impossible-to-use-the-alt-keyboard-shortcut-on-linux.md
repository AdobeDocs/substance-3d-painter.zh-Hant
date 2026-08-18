---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/technical-issues/miscellaneous-issues/impossible-to-use-the-alt-keyboard-shortcut-on-linux.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中解決 Linux 上 ALT 鍵盤快捷鍵的問題，以正確操作鍵盤。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Miscellaneous Issues > Impossible to use the ALT keyboard shortcut on Linux
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Linux 上無法使用 ALT 鍵盤快捷鍵
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---


# Linux 上無法使用 ALT 鍵盤快捷鍵

如果你使用的是使用 Gnome **作為使用者介面的 Linux 發行版（** Ubuntu **或** CentOS **），你可能想關閉 ALT** 鍵的&#x200B;**預設行為，以便在視窗中導航。**

## CentOS

1 - 進入  **系統> Windows**

![](../../../assets/centos-window.png){width="250px"}

2 - 將「移動鍵」設定改成「Alt **」以外的**&#x200B;設定。例如使用「  **Super**  」（選擇鍵盤上的「Windows」鍵）。

![](../../../assets/centos-setting.png){width="350px"}

## Ubuntu

1 - 開啟終端機並執行以下指令：

```
sudo apt-get install dconf-tools
```


這會安裝一個進階設定工具，你可能需要允許安裝額外的相依套件才能執行。

2 - 打開開始選單，尋找「  **Dconf-tools**  」。 發射。

3 - 透過以下路徑展開左側的樹狀選單：  **org > gnome > desktop > wm > 偏好設定**

4 - 編輯「滑鼠按鈕修飾符」並更改其值。 設定或代替，但  *不要空*  著。 Super 是相當於「Windows」鍵的等價物。

![](../../../assets/ubuntu-setting.png){width="500px"}
