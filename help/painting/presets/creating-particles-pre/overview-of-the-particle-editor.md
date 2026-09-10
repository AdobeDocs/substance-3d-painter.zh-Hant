---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/painting/presets/creating-particles-presets/overview-of-the-particle-editor.html"
breadcrumb-title: ''
description: 了解 Substance 3D Painter 中的粒子編輯器，以建立自訂的材質畫筆預設。
helpx_creative_field: ""
helpx_description: Painter > Painting > Presets > Creating particles presets > Overview of the particle editor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 粒子編輯器概述
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '1677'
ht-degree: 0%

---


# 粒子編輯器概述

本頁涵蓋 PopcornFX 粒子編輯器的多個面向。 部分視窗標題和參數可能會根據所使用的編輯器版本而有所變動。

## 視窗設定

### 如何匯入你自己的網格

把你的網格複製貼上到你的包裡的「Meshes」資料夾。 接著在編輯器裡打開你的網格，點選「建構」。

現在，在你的粒子系統中，進入樹狀檢視的「背景」，右鍵點選「3D Layers」、「New Backdrop」、「CNEdEditorBackdrop\_Model3D」，然後在「資源模型」中選擇你的網格。

在 Substance 3D Painter 中，網格會縮放成一個大小為 [-1;1] 的方框，每個軸上都是如此。 要在編輯器裡用 Substance 3D Painter 找到正確的縮放，你應該匯入已經縮放好、能放進那個框裡的網格（很簡單），或者在編輯器裡調整縮放。

注意：僅支援 FBX 網狀格式。

#### 如何顯示格子

Ctrl-G。你可以在「Editor Properties」裡的「GridColor」裡自訂格子的顏色。

## 發射極

### 如何建立「OnCollide」事件

Physics Evolver 負責場景中背景網格的碰撞。 在 Substance 3D Painter 中，場景就是你的網格。

首先在物理進化器中，將「WorldInteractionMode」設為「OneWay」以啟用粒子碰撞。 接著建立一個叫做「OnCollide」的事件，物理進化器會在與場景碰撞時觸發它。

在 Substance 3D Painter 中，場景就是你正在處理的模型，所有稱為「OnCollide」的事件都會被目前筆刷的發射粒子系統覆蓋。

#### 如何從相機發射粒子

在視窗頂端，啟用第四個按鈕「限制在攝影機平面上生成」。

Substance 3D Painter 預設會從攝影機發射發射器。

#### 如何在頂部發射像雨一樣的粒子

如果啟用了，請關閉「限制攝影機平面上的生成」。

建立一個名為「Global」的粒子屬性，Substance 3D Painter 會在原點生成你的粒子。

要在網格頂端生成，請新增一個形狀取樣器箱（BOX 或 CYLINDER），放在上面，然後在生成器腳本中取樣。

例如，對於一個名為「Spawn」的形狀取樣盒，可以把這個加到你的生成器腳本裡：

*Position = Spawn.samplePosition（）;*

## 接收器

### 如何在創建/編輯接收器時生成發射器

為了更接近 Substance 3D Painter 的工作流程，編輯接收器時可以設定編輯器來覆蓋生成的粒子系統。

在接收器的樹狀檢視中，選擇「編輯器屬性」，然後啟用「使用者超刷」，並在「超刷效果」中選擇你的發射器。

你仍然必須打開發射器，設定「OnCollide」事件來生成你目前正在編輯的接收器。

#### 如何設定粒子場

以下是你必須在接收器中擁有的粒子場描述：

*「尺寸」浮車*

Substance 3D Painter 中筆刷尺寸的乘法器。

*「不透明」浮車*

Substance 3D Painter 中筆刷不透明度的乘法器。

*「UV」float3*

就是粒子網格上的貼圖座標。

在 Evolver 腳本中，取樣你的形狀取樣器「網格」，並依據投影進化器給出的參數座標：

UV = Mesh.sampleTexcoord（pCoords）;

*「正常」float3*

粒子下方網格表面的法線。

在 Evolver 腳本中，取樣形狀取樣器「網格」，並以投影進化器給出的參數座標：

Normal = normalize（Mesh.sampleNormal（pCoords））;

*「種子」智力*

只是 Substance 3D Painter 隨機產生的數值：

在進化者腳本中添加：

種子 = int（rand（0,20000000））;

*「p座標」 int3*

Substance 3D Painter 沒有使用，但對於在網格上做粒子投影和其他場的取樣是不可或缺的。

#### 如何將粒子投影到網格上

在接收器的「狀態\_0」中加入投影進化器。

每幀，投影進化器會將粒子投射到形狀取樣器最近的表面。

投影進化器可在「OutputParametricCoordsField」指定的粒子場中填補投影的參數座標（參見「pCoords」粒子欄位）。

而且它可以用「ReprojectedField」在網格表面重新投影一個向量。

在這裡，我們想在 Sampler Shape 的「Mesh」上投影粒子，在 int3 粒子欄位的「pCoords」中填入參數座標，並在表面上投影「Velocity」：

#### 如何取樣網格

在 Substance 3D Painter 中，所有名為「Mesh」和「ShapeType」的形狀取樣器「MESH」都會被 Substance 3D Painter 所用的網格覆蓋。<b>\
</b>

在編輯器裡，設定成和背景相同的網格。

要在腳本中取樣，只要在腳本中寫「Mesh.sample~Something~（pCoords）」，以下是文件說明：

<https://wiki.popcornfx.com/index.php/CParticleSamplerShape#Script_bindings>

你需要一些有用的程式碼片段：

```
// UV is the texture coordinate of the particle on the mesh

// Must be after CParticleEvolver_Projection

UV = Mesh.sampleTexcoord(pCoords);

// Normal is the Normal of the surface on the mesh just below the particle

// Must be after CParticleEvolver_Projection

Normal = normalize(Mesh.sampleNormal(pCoords));
```


## 一般建議

### 如何在 Substance 3D Painter 中匯入發射器/接收器

在 Substance 3D Painter 裡，選擇「檔案」>「匯入粒子」或 Ctrl-Alt-R，然後在你的包裡選擇你的 Emitter.pkfx 或 Receiver.pkfx。

Substance 3D Painter 會自動偵測需求（粒子場、OnCollide 事件），判斷你的 pkfx 是發射器、接收器還是不相容。

現在，你應該會看到你的發射器/接收器放在架子上。

#### 如何除錯具有可行粒子大小的粒子

由於在 Substance 3D Painter 中，「Size」粒子欄位必須介於 0 和 1 之間，才能成為筆刷尺寸的乘數，因此在編輯器中粒子會過大。 所以，在生成器腳本中新增一個自訂欄位浮點數「BBSize」，設定為 0.01，在 Billboard 粒子渲染器中作為「SizeField」使用，以便更好地看到粒子。

#### 如何避免搞砸進化者順序

進化者的順序非常重要。

舉例來說，你可能想讓最後兩個演化器先是投影演化器，接著是腳本演化器，後者會取樣 UV 和法線，搭配投影演化器產生的 pCoordinates。

請記住，進化者的順序實際上就是影格內執行的順序，而 Substance 3D Painter 會收集粒子場值和每影格的結束。

#### 如何取樣網格的法線貼圖

Substance 3D Painter 會將所有稱為「NormalMap」的貼圖取樣器替換成網格的法線貼圖（如果已匯入）。

目前你只能用那個材質，其他材質都無法被 Substance 3D Painter 存取。

當你新增了名為「NormalMap」的貼圖取樣器後，可以用腳本取樣：

<http://www.popcornfx.com/wiki/index.php/CParticleSamplerTexture>

以下是一些實用的程式碼片段：

```
// In Evolver Script convert the NormalMap texture in tangent space to world space normal

// /!\ the "Normal" particle field must always be the normal of the mesh not influenced by the normal map

// /!\ dont forget to initialize your particle fields in your Spawn Script

// otherwise pCoords and Normal will be invalid at the first update

float normalFactor = 1.0; // change the intensity of the normal map

float3 meshnormal = Normal;

float4 rawtangent = Mesh.sampleTangent(pCoords);

float3 binormal = normalize(cross(meshnormal, rawtangent.xyz) * rawtangent.w);

float3 tangent = normalize(cross(meshnormal, binormal));

float3 tsNormal = normalize(((NormalMap.sample(UV).xyz * 2.0 - 1.0).xyz) * float3(-normalFactor, normalFactor, 1));

float3 normal = normalize(tsNormal.x * tangent + tsNormal.y * binormal + tsNormal.z * meshnormal);
```


#### 如何製造湍流

在編輯器中建立一個湍流取樣器。

<http://www.popcornfx.com/wiki/index.php/CParticleSamplerProceduralTurbulence>

接著你有兩種方式可以取樣湍流並影響粒子：

##### 簡單的方法

在你圖層的物理進化器中，將「VelocityFieldSampler」設為你的湍流取樣器名稱，並將「拖曳」設為 0 >。

##### 參數化方法

你可以透過取樣 Evolver 腳本中湍流取樣器產生的速度場來調整湍流：

建立兩個粒子屬性：

* float「TurbulencePower」最小值：[0;5]
* float 「TurbulenceScale」最小極大值：[0.001; 5]（需要> 0）

接著建立三個粒子場：

float 「TurbPower」與float 「TurbScale」

要在生成器腳本中儲存屬性：

* 渦輪尺度 = 1.0 / 湍流尺度;
* 渦輪功率 = 湍流功率;

float3 「VelocityField」在旋轉模式中。

它將作為物理進化器中的「VelocityField」（預設已設定為「VelocityField」）。

所以在使用物理進化器之前，先在腳本進化器中取樣你的湍流取樣器，名為「渦輪」：

VelocityField = Turb.sample（Position \* TurbScale） \* TurbPower;

#### 如何正確使用 dt，也就是 delta 時間

Delta 時間是指每次影格更新之間的模擬時間（以秒數計）。 在編輯器中，delta 時間會更新為實際經過時間。 在 Substance 3D Painter 中，delta 時間是固定的，每次更新完成後都會立即啟動。

一款以 60 FPS 運行的遊戲，差值時間約為 1/60 = 0.016 秒，所以盡量讓筆刷在 0.016 秒左右運行。

* 大變化時間>0.016秒
* PRO 快速更新

由於更新間隔較長，粒子的移動會變大，因此 Substance 3D Painter 的筆刷會跑得更快。

* CON 近似

PopcornFX 是一種大型離散化系統，DT 越大，不精確度也會越大。 參見湍流中大 delta 時間的意涵： <http://www.popcornfx.com/wiki/index.php/CParticleEvolver_Physics#Dealing_with_turbulences_at_low_framerates>

* 體質（CON splats）

如果 delta 時間很長，畫面間粒子移動也會很大。 所以在《Substance 3D Painter》中，可能會出現小點而不是直線。

這是因為 Substance 3D Painter 會在每幀結束時為每個粒子畫一個筆劃點，且不會在上一幀和當前幀之間為每個粒子畫線。

* 小三角洲時間 &lt; 0.016s
* PRO 精度

變小的時間越短，筆觸間距越小，畫出來的畫面也會更銳利。 模擬的離散化也會更好。

* CON 慢

delta 時間越小，繪製相同距離所需的更新次數越多。

關於 delta 時間的最後建議：一個好方法是從大 dt（0.1 秒）開始，然後逐步減少，達到你想要的結果。

#### 如何揭露粒子系統的參數

Substance 3D Painter 將收集粒子系統的粒子屬性，並以 Physic Brush 參數顯示：

<http://www.popcornfx.com/wiki/index.php/Particle_effect_attributes>

在 PopcornFX 裡，你有一個叫做「Evolution 屬性」的功能，可以讓你在 Evolve 腳本中存取屬性：千萬不要這麼做。 相反地，先建立粒子欄位並在生成器腳本中儲存屬性，然後在 Evovler 腳本中使用這些粒子欄位。 （這點未來可能會修正）

#### 如何偵測有問題的粒子

你絕對不應該讓粒子場值異常，所以偶爾要在有問題的狀態下斷開：

<http://www.popcornfx.com/wiki/index.php/Particle_tips_BreakOnProblematicParticle>

#### 如何在 Substance 3D Painter 中解決粒子系統問題

在 Substance 3D Painter 安裝目錄中，你應該會找到一個叫做「popcorn.htm」的檔案。 這個檔案包含了 PopcornFX 的所有日誌，請打開裡面看看可能發生什麼問題。

#### 如何正確初始化粒子場

要取得第一幀有效的 pCoords UV 和法線，請將以下內容加入你的生成器腳本：

<b>  
</b>

```
// PostEval() will be called after particles have been translated to their respective spawn locations

// so, PostEval() is executed in world space

function void PostEval()

{

// we need to initialize correctly the values needed by Substance 3D Painter:

pCoords = Mesh.projectParametricCoords(Position);

UV = Mesh.sampleTexcoord(pCoords);

Normal = normalize(Mesh.sampleNormal(pCoords));

}
```
