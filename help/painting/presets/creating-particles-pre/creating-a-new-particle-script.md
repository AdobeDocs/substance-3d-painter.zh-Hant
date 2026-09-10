---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/painting/presets/creating-particles-presets/creating-a-new-particle-script.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中建立新的粒子腳本，以定義自訂的粒子筆刷行為與效果。
helpx_creative_field: ""
helpx_description: Painter > Painting > Presets > Creating particles presets > Creating A New Particle Script
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 建立新的粒子腳本
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '728'
ht-degree: 0%

---


# 建立新的粒子腳本

下載預先設定好的 PopcornFX 套件： [模板\_EmitterReceiver.pkkg](https://helpx.adobe.com/content/dam/help/en/substance-3d/documentation/spdoc/files/67403778/68419585/1/1411557944000/templates-emitterreceiver.pkkg)

這個套件是一個「起始套件」，包含發射器和接收器，我們將在 Substance 3D Painter 中編輯並匯入。

## 爆米花效果器材設定

啟動 PopcornFX Editor，建立一個新專案，然後打開它。

在你的專案中，右鍵點擊一個空白區域，選擇「匯入爆米花套件」。 然後選擇「範本\_EmitterReceiver.pkkg」。

現在，你應該要：

* 一個粒子系統「\_Emitter」，是發射體的基底模板。
* 一個粒子系統「\_Receiver」，是接收器的基礎模板。
* 一個球體網格作為場景的預設背景

「\_Emitter」和「\_Receiver」已經是「畫家準備好了」。 他們已經配置好必要的進化器、場域、背景等等......

## 匯入你的網格

PopcornFX 只支援  **FBX**  ，記得匯出你的網格時要用這個格式。 在匯出階段，檢查你的網格大小，試著在「真實世界」中用正確的單位。

複製貼上到你專案的「meshes」資料夾（在 PopcornFX 裡，你可以右鍵點擊「meshes」資料夾，選擇「開啟檔案位置」）。

回到編輯器，打開你的網格（雙擊它），然後點選「  **建造**  」。 關掉視窗，存起找零。

## 發射極/接收端編輯

我們將複製現有粒子系統，並調整以正確納入新網格。

右鍵點擊粒子系統「\_Emitter」（在「Particles」資料夾中），選擇「複製」（或「複製」）來建立你自己的發射器。

打開它，在「粒子樹檢視」視窗（左下角）選擇「  **Layer\_Model**  」，該視窗應該位於：「Editor Properties => Backdrop => 3D Layers」。

然後在「Node Properties」視窗裡，把「dummymesh.fbx」替換成你的模型。 儲存修改（File => Save）並關閉發射器視窗。

現在，複製  **「\_Receiver**   **」（**  在「Particles」資料夾裡），用這個建立你自己的接收器。

打開它，至於發射器，請用你的模型在「Layer\_Model」中替換假網格。 我們修改了螢幕上顯示的網格&#x200B;**&#x200B;**，但同時也需要修改&#x200B;**粒子所使用的網格**&#x200B;**。**&#x200B;**&#x200B;**      

要做到這點，在「粒子樹狀檢視」視窗中，點選「  **形狀**  」，應該位於：「粒子效果 => Spawner => Layer\_1 => Samplers => 網格」。

然後，將「MeshResource」替換成你的模型。

完成後，還有最後一件事要做：我們需要將發射極和接收器與剛建立的發射器「連結」。

在接收器的樹狀檢視中，選擇「編輯器屬性」，然後在「OverSpawnEffect」中選擇你的發射器。 救回接收器。

打開你的發射器（我們之前複製的那個），在「粒子樹檢視」視窗中點選「事件」，該視窗應該位於：「粒子效應 => 生成器」。 然後點選「Extern」，把接收機換成你的接收器。\
完成了！ 現在如果你選擇 3D 視角（發射器或接收器），你可以按「空白」按鈕來建立粒子。

## 可選：修改接收者的行為

打開接收器，在「Particles Treeview」視窗中，選擇「CParticleEvolver\_Script」（最上面專門給:)你的那個），應該位於：「Particle Effect => Layer\_1 => State\_0」。

在「專用節點編輯器」視窗中，函式中加入「Life = 0.5;」以改變粒子壽命。 然後用「Ctrl+s」捷徑儲存你的腳本。 你應該能在 3D 視角中察覺差異。

欲了解更多運作方式，請造訪以下連結：

<http://wiki.popcornfx.com/index.php/Main_Page>

## Substance 3D Painter 中的匯入發射器/接收器

在 Substance 3D Painter 裡，請選擇「檔案」>「匯入粒子」或 Ctrl-Alt-R，然後在你的 Pack 裡選擇發射器和接收器（兩者皆為 .pkfx 格式）。

Substance 3D Painter 會自動偵測需求（粒子場、OnCollide 事件），判斷你的 pkfx 是發射器、接收器還是不相容。

現在，你應該會在架子裡看到你的發射極/接收器（在「發射器」和「接收器」分頁）。

要使用它們，你首先需要點擊「切換粒子」按鈕。

接著，在「工具」視窗的「物理」中，你可以選擇發射器（取代「default\_emitter」）和接收器（取代預設_receiver）。

你現在可以在「工具」視窗中右鍵點擊並儲存工具。
