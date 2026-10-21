---
breadcrumb-title: ''
description: 檢視 Substance 3D Painter 版本的所有變更與更新，以追蹤功能隨時間的演進與改進。
title: 所有變動
user-guide-description: ''
user-guide-title: ''
source-git-commit: 479eb327180dd223bbff362e3f200995565cbcfa
workflow-type: tm+mt
source-wordcount: '40713'
ht-degree: 0%
---

# 所有變動

本頁包含所有先前 Substance 3D Painter 發行的發行說明，依序從最新到最舊排序。

>[!NOTE]
>
> 欲查看可能影響 Painter 的已知問題，請參閱 [專門的文件頁面](known-issues.md)。

## 版本 12

### 12.2.0

上映日期： **2026/10/21**

摘要： **這次更新是重大更新，新增了烘焙籠子繪畫功能，並改進了多邊形填充功能。 更多細節請參閱完整的發行說明。**

**補充：**

* 烘焙、籠子畫
* &amp;lbrack;籠子繪畫&amp;rbrack; 建立基本的籠子繪畫介面
* &amp;lbrack;籠子繪畫&amp;rbrack;新的籠子視覺化選項
* &amp;lbrack;籠子繪畫&amp;rbrack;可編輯選取/填充工具
* &amp;lbrack;籠子繪畫&amp;rbrack;工具列顯示混合模式
* &amp;lbrack;籠子繪製&amp;rbrack;HDR 滑桿介面變更
* &amp;lbrack;籠子繪畫&amp;rbrack;視覺化著色器
* &amp;lbrack;籠子塗裝&amp;rbrack;重置堆疊選項
* 多邊形填充工具的改進
* &amp;lbrack;多邊形填充&amp;rbrack;新增多邊形補丁
* &amp;lbrack;多邊形填充&amp;rbrack;新增多邊形迴圈
* &amp;lbrack;多邊形填充與rbrack;對稱性支援與 Loop/Patch
* &amp;lbrack;多邊形填充&amp;rbrack;對稱邊緣預覽
* &amp;lbrack;多邊形填充&amp;rbrack;移除帶有環狀和部分環狀的三角形
* &amp;lbrack;多邊形填充&amp;rbrack;線框僅顯示於啟用的材質集
* &amp;lbrack;Polygon fill&amp;rbrack;不可點擊三角形上的紅色邊緣高亮
* &amp;lbrack;Polygon fill&amp;rbrack;不要關閉填充模式選項
* &amp;lbrack;多邊形填充&amp;rbrack;允許以多邊形填充設定所有通道屬性
* &amp;lbrack;Polygon Fill&amp;rbrack;恢復前一筆劃，使用 Polygon Fill
* &amp;lbrack;Polygon fill&amp;rbrack;在非活動材質集上顯示禁止游標
* &amp;lbrack;Polygon Fill&amp;rbrack;ALT 即時預覽
* &amp;lbrack;Polygon Fill&amp;rbrack;臨時切換到 Polyloop（SHIFT+A） 的捷徑
* &amp;lbrack;Viewport&amp;rbrack; 顯示材質集 / UV 圖塊選取高亮
* &amp;lbrack;Viewport&amp;rbrack; 新增即時視窗中對訂單獨立透明度的支援
* &amp;lbrack;顯示設定&amp;rbrack;將顯示設定重新組織成新群組
* &amp;lbrack;Tool&amp;rbrack;新增筆觸加法混合的支援
* &amp;lbrack;Tool&amp;rbrack;新增多邊形填充的加法混合支援
* &amp;lbrack;USD&amp;rbrack;匯出的美元搭配不透明度地圖在 Arnold 中渲染全透明
* &amp;lbrack;Nvidia&amp;rbrack;新增關於最新 Nvidia 驅動程式（616.56 至 617.14）的警告
* 新增新的「mesh_uv_neighbor」引擎貼圖輸入
* 將 Baker 更新至 3.23.0 版本
* 更新 Substance 引擎至 9.6.1 版本

**修正：**

* &amp;lbrack;Baking&amp;rbrack; 環境遮蔽 忽略 mesh 名稱的背面無法運作
* &amp;lbrack;烘焙&amp;rbrack; &amp;lbrack;AMD&amp;rbrack;在使用重高多邊形網格烘焙時裝置遺失
* &amp;lbrack;Performances&amp;rbrack; Painter 佔用 VRAM 的使用
* &amp;lbrack;Viewport&amp;rbrack;在 HDPI 螢幕上開啟專案時缺少貼圖
* &amp;lbrack;工具&amp;rbrack;在遮罩中繪製時，混合模式會顯示灰色
* 匯出網路後暫存資料夾未被刪除
* &amp;lbrack;USD&amp;rbrack;出口的美元幾何形狀沿 UV 邊界劃分
* &amp;lbrack;USD&amp;rbrack;載入畸形USDz時凍結

### 12.1.5

上映日期： **2026/09/15**

摘要： **小規模發行**

**修正：**

* 從書架匯出映像到網路已經無法運作了
* &amp;lbrack;Generator&amp;rbrack;將「use texture」設為 false 並不會禁用材質輸入的使用。
* 在編輯 3D 投影時儲存視窗會凍結
* 材質分層解析度太低

### 12.1.4

上映日期： **2026/09/04**

摘要： **小規模發行**

**修正：**

* &amp;lbrack;Crash&amp;rbrack;匯入或匯出檔名非 ASCII 字元的檔案時會當機

### 12.1.3

上映日期： **2026/08/26**

摘要： **小規模發行**

**補充：**

* 更新 Substance 引擎至 9.4.6 版本

**修正：**

* &amp;lbrack;灰階 picker&amp;rbrack;更換工具後 Picker 仍保持開啟
* &amp;lbrack;Schow Baking&amp;rbrack;上色和解除時，Schew 修正會斷裂
* &amp;lbrack;投影工具&amp;rbrack;投影工具阻擋視窗互動
* &amp;lbrack;動態筆劃&amp;rbrack;筆刷屬性中缺少動態筆劃參數
* 匯出到網路已經無法再運作了

### 12.1.2

上映日期： **2026/08/03**

摘要： **小規模發行**

**修正：**

* &amp;lbrack;Crash&amp;rbrack;有些物質在渲染時可能導致崩潰
* &amp;lbrack;Crash&amp;rbrack;在烘焙模式下重新匯入網格
* &amp;lbrack;當機&amp;rbrack;未初始化圖形顯示可能導致當機
* &amp;lbrack;Crash&amp;rbrack;匯出貼圖有時會在更新日誌時當機
* &amp;lbrack;Crash&amp;rbrack;在載入或更新環境貼圖時，烘焙模式會崩潰
* &amp;lbrack;Baking&amp;rbrack;修改高多邊形檔案後重新啟動烘焙可能會導致當機
* &amp;lbrack;傳送到 Photoshop&amp;rbrack;無法匯出圖層遮罩
* &amp;lbrack;Engine&amp;rbrack;錨點結果不會在遮罩和色彩通道之間渲染

### 12.1.1

發行日期： **2026/07/09**

摘要：小規模發行

補充：

* &amp;lbrack;斜烘焙&amp;rbrack;露出斜斜基礎法線模式：網格或每三角形
* &amp;lbrack;Properties&amp;rbrack; 讓統一顏色總是重置為其通道的預設值
* &amp;lbrack;OpenPBR&amp;rbrack;在輸出材質視窗中依類別重新組合通道以建立輸出範本
* 更新 Substance 引擎至 9.4.5 版本

修正：

* &amp;lbrack;Project&amp;rbrack;開啟和保存某些專案會比平常花更長時間
* &amp;lbrack;Crash&amp;rbrack;重裝多個網格可能導致崩潰
* &amp;lbrack;Crash&amp;rbrack;在遮罩檢視模式下刪除通道會導致當機
* &amp;lbrack;Crash&amp;rbrack;有些物質在渲染時可能導致崩潰
* &amp;lbrack;Paint Skew&amp;rbrack;在切換到繪畫模式後，所選工具仍保持選取
* &amp;lbrack;烘焙常用設定&amp;rbrack;籠子距離設定不會更新籠子線框和著色器視覺化
* &amp;lbrack;Engine&amp;rbrack; UV 填充「3D 空間鄰居」模式在細三角形上效果不佳
* &amp;lbrack;Engine&amp;rbrack;錨點結果不會在遮罩和色彩通道之間渲染

### 12.1.0

上映日期： **2026/06/23**

摘要： **這次更新是重大更新，包含 Baker 的改進，包括新的烘焙預設 UI 狀態、繪製斜面貼圖、自動重新烘焙、硬表面網格自動 UV 展開選項，以及 OpenPBR。 更多細節請參閱完整的發行說明。**

**補充**：

* &amp;lbrack;Skew 烘焙&amp;rbrack;Schew 繪畫工具
* &amp;lbrack;Skyw Baking&amp;rbrack; 在繪製斜面貼圖時新增斜度預覽著色器和斜向量視覺效果
* &amp;lbrack;傾斜烘焙&amp;rbrack;新增邊緣保護選項
* &amp;lbrack;Schow baking&amp;rbrack;自動重新烘焙
* &amp;lbrack;Skew Baking&amp;rbrack;重製網格地圖列表介面
* &amp;lbrack;傾斜烘焙&amp;rbrack; 分割網格貼圖 / 常見烘焙設定 + 將共用設定從網格貼圖列表中移出底色或僅遮罩
* &amp;lbrack;Skew Baking&amp;rbrack; Change viewport toolbar button
* &amp;lbrack;斜向烘焙&amp;rbrack;顯示頂部工具列筆刷對稱切換
* &amp;lbrack;Skyw Baking&amp;rbrack;網格地圖中的重命名選項 列表同步選單
* &amp;lbrack;Skew Baking&amp;rbrack;更新同步與檢查狀態對話框
* &amp;lbrack;Skyw Baking&amp;rbrack; 建立灰階色彩選擇器變體
* &amp;lbrack;Skew Baking&amp;rbrack; 更新烘焙模式圖示
* &amp;lbrack;自動展開&amp;rbrack;整合硬表面選項
* &amp;lbrack;OpenPBR&amp;rbrack;新增對 OpenPBR 1.1 的支援
* &amp;lbrack;OpenPBR&amp;rbrack;讓 OpenPBR 成為預設工作流程與著色器
* &amp;lbrack;OpenPBR&amp;rbrack;透過美元匯入 OpenPBR 材質與材質
* &amp;lbrack;OpenPBR&amp;rbrack;透過美元匯出 OpenPBR 材質與材質
* &amp;lbrack;OpenPBR&amp;rbrack;更新匯出材質視窗以顯示 OpenPBR 命名規則
* &amp;lbrack;OpenPBR&amp;rbrack;新增有關支援 OpenPBR 變更的文件
* &amp;lbrack;OpenPBR&amp;rbrack;&amp;lbrack;Iray&amp;rbrack; 新增 MDL 以支援 Iray 中的 OpenPBR 1.1
* 美元出口的多項小幅改善
* &amp;lbrack;UI&amp;rbrack; 嘗試在另一個材質集上繪製時，在視窗中新增警告
* &amp;lbrack;Flatten&amp;rbrack; 允許在材質集上將所有實例化圖層壓平
* &amp;lbrack;紋理設定設定&amp;rbrack; 允許透過新視窗同時選擇多個頻道
* &amp;lbrack;History&amp;rbrack; 更新「value」 還原條目措辭以反映參數名稱
* &amp;lbrack;Layer stack&amp;rbrack; 將遮罩中的填充效果預設為白色（1.0）
* &amp;lbrack;Substance&amp;rbrack; 新增「mesh_hard_edges_triangle」引擎地圖輸入
* &amp;lbrack;Substance&amp;rbrack; 新增「mesh_hard_edges」引擎地圖輸入
* &amp;lbrack;Shader&amp;rbrack; 防止著色器實例共享相同名稱
* &amp;lbrack;Shader&amp;rbrack;匯入 USD 或 GLTF 檔案時，請使用專案範本中的著色器
* 將 Adobe Color Engine 更新至 7.0 版本
* 將 MacOSX 最低版本升級到 13.0（Ventura）
* &amp;lbrack;內容&amp;rbrack;OpenPBR 新專案範本
* &amp;lbrack;內容&amp;rbrack;更新範例專案以使用新的 OpenPBR 著色器
* &amp;lbrack;Python&amp;rbrack;擴展幾何遮罩 API，允許像 UI 一樣的包含與排除模式

**修正**：

* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;網格映射設定&amp;rbrack; 套用設定到其他材質集
* &amp;lbrack;Crash&amp;rbrack;當從地圖烘焙曲率時，沒有世界空間法線
* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Baking&amp;rbrack; 啟用自訂籠子但未選取檔案的烘焙 當機
* &amp;lbrack;Crash&amp;rbrack;取消AO烘焙
* &amp;lbrack;自動籠子與rbrack;當高多邊形檔案路徑無效時，無限載入
* &amp;lbrack;Linux&amp;rbrack;&amp;lbrack;Windows&amp;rbrack; 顏色選擇器有時會完全呈現黑色或不顯示
* &amp;lbrack;多邊形填充工具&amp;rbrack;此工具無法支援非 PBR
* &amp;lbrack;&amp;lbrack;Paint&amp;rbrack; 刪除底色通道不會刪除先前繪製的顏色
* &amp;lbrack;USD&amp;rbrack;著色器實例並非全部正確偵測
* &amp;lbrack;Substance&amp;rbrack;僅考慮輸入/輸出節點的首次使用情況
* &amp;lbrack;Shader&amp;rbrack;環境遮蔽會用不同的混音方法，透過紋理集套用兩次
* &amp;lbrack;Engine&amp;rbrack;法線貼圖中藍色通道（黑色）空的，可能會導致錯誤的混合結果
* &amp;lbrack;GLTF Import&amp;rbrack;每個貼圖集都啟用了 Alpha 混合
* &amp;lbrack;GLTF Export&amp;rbrack;Alpha 混合在匯出時始終啟用
* &amp;lbrack;Export&amp;rbrack;匯入 GLTF 檔案時，雙面幾何總是被禁用
* &amp;lbrack;Javascript&amp;rbrack;修改著色器設定不會影響還原歷史紀錄
* &amp;lbrack;Samples&amp;rbrack;Meet Mat 的顯示設定中未啟用地下散射

### 12.0.3

上映日期： **2026/05/05**

摘要： **小規模發行**

**補充：**

* 將 Bakers 更新至 3.22.2 版本
* 將 Substance 引擎更新至 9.4.3 版本
* &amp;lbrack;Python&amp;rbrack;將智慧素材儲存到特定位置

**修正：**

* &amp;lbrack;Ubuntu&amp;rbrack;選擇素材時崩潰
* &amp;lbrack;Mac&amp;rbrack;反覆彈出視窗似乎會詢問存取其他應用程式資料
* &amp;lbrack;Baking&amp;rbrack;文物可以出現在曲率地圖上
* &amp;lbrack;烘焙&amp;rbrack;烘焙在某些情況下較慢
* &amp;lbrack;warp to geometry&amp;rbrack; warp to geometry 在某些情況下會被禁用
* &amp;lbrack;UV Tile&amp;rbrack;錨點提取的 alpha 被其他 tile 忽略
* &amp;lbrack;Python&amp;rbrack;&amp;lbrack;Mac&amp;rbrack; Python console with SSL 中的例外
* &amp;lbrack;Python&amp;rbrack; Painter 在 exit 時 crash with leftover Qt widgets

### 12.0.2

上映日期： **2026/04/07**

摘要： **小規模發行**

**補充：**

* &amp;lbrack;色彩管理&amp;rbrack; 新增 OCIO 以指定色彩選擇器的預設色彩空間
* &amp;lbrack;Python&amp;rbrack; Expose auto-unwrap settings in Python API

**修正：**

* &amp;lbrack;Crash&amp;rbrack;磁碟空間不足的儲存可能會當機或損壞專案
* &amp;lbrack;Crash&amp;rbrack; &amp;lbrack;Ribbon&amp;rbrack;使用Ribbon可能會導致某些專案當機
* &amp;lbrack;當 .assbin 檔案無法寫入資料夾時，當 crash
* &amp;lbrack;Import&amp;rbrack;Stager 的 OBJ 網格在建立專案時可能會失敗
* &amp;lbrack;進口&amp;rbrack;OBJ 在某些情況下會缺少臉
* &amp;lbrack;Import&amp;rbrack;未分配材質的美元網格可能會在匯入時當機
* &amp;lbrack;填充路徑&amp;rbrack;不受對稱性影響
* &amp;lbrack;模板&amp;rbrack;預覽解析度低於繪製結果
* &amp;lbrack;UI&amp;rbrack;「uv island」仍被提及於 ID 地圖色彩來源提示中
* &amp;lbrack;顯示&amp;rbrack;陰影呈現反轉
* &amp;lbrack;Viewport&amp;rbrack;切換到烘焙模式後，Warp 投影轉換仍會保留
* &amp;lbrack;Warp&amp;rbrack;當 Z 軸縮放為 0，且啟用 Warp to geometry 時，網格會消失
* &amp;lbrack;Python&amp;rbrack;新增帶有 Scoped 修改的通道時出現意外錯誤

### 12.0.1

上映日期： **2026/03/18**

摘要： **小規模發行**

**修正：**

* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Freeze&amp;rbrack;從特定專案出口

### 12.0.0

發行日期： **2026/03/09**&#x200B;摘要： **這是一本重大發行。 此版本包含圖層扁平化、幾何變形、新後製效果、新專案視窗改進及其他改進功能。**

**補充**：

* &amp;lbrack;將圖層平整&amp;rbrack;將圖層堆疊內的圖層壓平
* &amp;lbrack;平整圖層&amp;rbrack;將扁平圖層匯出至磁碟
* &amp;lbrack;Warp to geometry&amp;rbrack; 新增自動 Warp 投影功能
* &amp;lbrack;後製效果&amp;rbrack;用新增後效替換後期效果
* &amp;lbrack;Post-effects&amp;rbrack; 更新音調映射器
* &amp;lbrack;Post-effects&amp;rbrack; 新增後效資產用法
* &amp;lbrack;內容&amp;rbrack;&amp;lbrack;Post-effects&amp;rbrack; 將預設後期效果資產整合到函式庫中
* &amp;lbrack;新專案&amp;rbrack;改善專案建立介面
* &amp;lbrack;新專案&amp;rbrack;重新匯入網格功能的變更
* &amp;lbrack;新專案&amp;rbrack;允許開啟 \*.geo.usd 檔案
* &amp;lbrack;專案配置&amp;rbrack;改善專案配置介面
* 將 USD 函式庫更新至 25.05 版本
* 更新 Substance Engine 至 9.3.4 版本
* AMD GPU 的最低驅動程式提升到 25.3.1/25.Q2
* 更新Qt至6.8.6
* &amp;lbrack;Scripting&amp;rbrack; 更新JavaScript API至版本1.1.20
* 將 Python 更新至 3.13

**修正：**

* &amp;lbrack;Crash&amp;rbrack;在遮罩中更改材質通道輸出可能會崩潰
* &amp;lbrack;Import&amp;rbrack;匯入 USD 檔案時，EXR 材質會強制變成 sRGB 而非線性
* &amp;lbrack;UV 圖塊&amp;rbrack;單一影像的影像序列也會填充其他 UV 圖塊
* &amp;lbrack;Baking&amp;rbrack;AO 在 CPU 和 GPU 烘焙之間是不同的
* &amp;lbrack;色彩管理&amp;rbrack;&amp;lbrack;MacOS&amp;rbrack; Viewport BaseColor 不匹配 colorpicker
* &amp;lbrack;USD&amp;rbrack;統一價值在某些情況下不會進口

## 版本 11

### 11.1.3

發行日期： **2026/02/12**&#x200B;摘要： **次要發行**

**修正**：

* &amp;lbrack;Paint&amp;rbrack;模板和對稱在某些情況下無法運作
* &amp;lbrack;Path&amp;rbrack;更改模糊筆劃不透明度滑桿時沒有更新
* &amp;lbrack;Project&amp;rbrack;無法在某些幾何上繪製
* &amp;lbrack;Ribbon&amp;rbrack;當更改貼圖集解析度時，實例化路徑會消失
* &amp;lbrack;UI&amp;rbrack;顏色選擇器在某些情況下會縮小甚至消失

### 11.1.2

上映日期： **2026/01/13**&#x200B;摘要： **次要發行**

**補充**：

* &amp;lbrack;Baking&amp;rbrack;透過非同步節省改善 UV Tiles 專案的烘烤時間
* &amp;lbrack;Shaders&amp;rbrack; 在 Shader API 變更日誌中提及 Vulkan 遷移後的變更
* 將 OpenEXR 更新至 3.4.4 版本

**修正**：

* &amp;lbrack;Crash&amp;rbrack;Nvidia GTX 10xx 系列啟動時當機
* &amp;lbrack;當機&amp;rbrack;在不同的材質集上使用顏色選擇器可能會導致退出應用程式時當機
* &amp;lbrack;Performance&amp;rbrack;在多層專案中上色時的效能問題
* &amp;lbrack;性能&amp;rbrack;用繪圖板筆繪畫時會延遲
* &amp;lbrack;UI&amp;rbrack;在渲染模式下（Iray）相機設定會保持關閉狀態。
* &amp;lbrack;Ribbon&amp;rbrack;路徑在某些情況下會在轉角後意外重疊
* &amp;lbrack;Ribbon&amp;rbrack;UV磁磚的效能問題
* &amp;lbrack;Substance&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 圖片輸入在摺疊時消失
* &amp;lbrack;Substance&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 巢狀群組即使 Visible If 隱藏它們，仍可保留
* &amp;lbrack;Baking&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 無法將曲率抽樣半徑設於 0.01 之外
* &amp;lbrack;烘焙&amp;rbrack;&amp;lbrack;UI&amp;rbrack;無法將最大Occluder 距離設定超過1
* &amp;lbrack;烘焙&amp;rbrack;AO 設定「自我遮蔽」在多個紋理設定和低為高烘焙時會被忽略
* &amp;lbrack;Baking&amp;rbrack;ID 映射不會在低模式下烘焙 FBX 的頂點顏色
* &amp;lbrack;內容&amp;rbrack;高通濾波器會導致色彩管理通道的顏色變淡

### 11.1.1

發行日期： **2025/12/09**&#x200B;摘要： **次要發行**

**補充**：

* &amp;lbrack;Performance&amp;rbrack; 在計算部分紋理時提升 UV 磁磚的效能
* &amp;lbrack;Bakers&amp;rbrack;更新至版本 3.15.4

**修正**：

* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;MacOS&amp;rbrack; 從前版本儲存專案總是當機
* &amp;lbrack;崩潰&amp;rbrack;關閉專案有時會導致崩潰
* &amp;lbrack;Project&amp;rbrack; 在開啟前版本專案時出現錯誤「成員計算不匹配」
* &amp;lbrack;烘焙&amp;rbrack;UV圖塊若存在，則不會與先前烘焙結果合併
* &amp;lbrack;Baking&amp;rbrack;即使在 Nvidia GTX 10XX 系列關閉光線追蹤，裝置仍遺失
* &amp;lbrack;Baking&amp;rbrack;AO 在普通模式中邊緣會有雜訊，因為沒有填充
* &amp;lbrack;Baking&amp;rbrack;AO 設定「自我遮蔽」會被忽略，因為多個材質集和「以名稱匹配」開啟
* &amp;lbrack;Baking&amp;rbrack;若有高多邊形網格缺少頂點顏色，ID Map 將完全呈現黑色
* &amp;lbrack;Ribbon&amp;rbrack;Alpha 混合模式的提示提到的是螢幕混合模式，而非線性閃避
* &amp;lbrack;Path&amp;rbrack;當點靠近路徑端點時，切線會產生意外迴圈
* &amp;lbrack;工具&amp;rbrack;材質預覽在遮罩中使用投影時無法運作
* &amp;lbrack;Engine&amp;rbrack;繪製小筆觸可能導致方塊狀的瑕疵
* &amp;lbrack;Shader&amp;rbrack;取消建立著色器實例時，該實例無法正確移除
* &amp;lbrack;Export&amp;rbrack;GLTF 匯出的 Alpha 模式總是設定為 MASK
* &amp;lbrack;Python&amp;rbrack;在超出範圍修改區塊外編輯圖層堆疊時，出現意外錯誤

**已知問題**：

* &amp;lbrack;Ribbon&amp;rbrack;UV磁磚的效能問題
* &amp;lbrack;Ribbon&amp;rbrack;路徑在某些情況下會在轉角後意外重疊
* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Ribbon&amp;rbrack; 在 Ribbon 中建立非常長的文字可能會當機
* &amp;lbrack;色彩管理&amp;rbrack;在 Linux 上使用 ACE 進行 HDR 色彩空間轉換會產生壓縮色彩
* &amp;lbrack;Regression&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 右鍵選單在 HD 螢幕上太小了
* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Python&amp;rbrack; USD export by TextureStateEvent 觸發
* &amp;lbrack;Engine&amp;rbrack;用克隆工具在正常通道色彩移位中繪製時，顏色移位錯誤
* &amp;lbrack;Python&amp;rbrack;Ghost 小工具似乎已被腳本刪除，但仍能運作

### 11.1.0

發佈日期：**2025/11/18**&#x200B;摘要：**此更新為重大更新，包含全新功能區工具及專屬內容、填充層對稱支援、位移物理尺寸參數、透過更新烘焙軟體提升效能、完整支援 Windows 與 Linux Vulkan 及其他改進。**

**補充**：

* 新的排帶工具
* &amp;lbrack;Tool&amp;rbrack; 新增 Ribbon 工具以打造無縫路徑
* &amp;lbrack;Ribbon&amp;rbrack; 在屬性視窗中新增 Ribbon 預設捷徑
* &amp;lbrack;Ribbon&amp;rbrack;允許在路徑上每個頂點改變緞帶的不透明度
* &amp;lbrack;Ribbon&amp;rbrack;允許在路徑上每個頂點改變色帶的大小
* &amp;lbrack;Ribbon&amp;rbrack;當路徑關閉時，移除實體中定義的開始/結束
* &amp;lbrack;Ribbon&amp;rbrack;在屬性視窗中移除 Paint/Eraser/Smudge 路徑工具的路徑/材質預覽
* &amp;lbrack;Ribbon&amp;rbrack;在自我重疊時為 alpha 和部分通道加入混合模式
* 填充對稱性
* &amp;lbrack;Fill&amp;rbrack;新增對填充層與效果對稱性的支援
* &amp;lbrack;Fill&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 在屬性視窗中揭露填充層與效果的對稱設定
* &amp;lbrack;Fill&amp;rbrack; 重新設計視窗選單和屬性視窗中的對稱設定介面
* &amp;lbrack;Fill&amp;rbrack;在warp模式下投影時，正確重新定位法線貼圖
* 物理尺寸位移
* &amp;lbrack;排水量&amp;rbrack;使用物理尺寸作為排水量單位
* 效能提升
* &amp;lbrack;Performance&amp;rbrack;改善大三角形上小筆觸的渲染
* &amp;lbrack;Performance&amp;rbrack;提升著色器編譯時間
* &amp;lbrack;Performance&amp;rbrack;Windows 與 Linux 的完整 Vulkan 支援
* &amp;lbrack;Performance&amp;rbrack;更新的烘焙軟體，提供更快的 GPU 渲染並支援 AMD 光線追蹤
* &amp;lbrack;UI&amp;rbrack;將工具屬性重新組織成群組，並預設部分內容會合併
* &amp;lbrack;Engine&amp;rbrack;將 Substance Engine 更新至 9.2.5 版本
* &amp;lbrack;Substance&amp;rbrack;工具與填充中對Substance資源的解析覆寫
* &amp;lbrack;Export&amp;rbrack; 更新網格貼圖匯出預設以匯出灰階貼圖
* Python
* &amp;lbrack;Baking&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 在變更日誌中顯示，在烘焙者更新後破壞變更
* &amp;lbrack;Python&amp;rbrack; 在 Python 中揭露填充對稱設定
* 內容與新內容
* &amp;lbrack;內容&amp;rbrack; 新增 75 個 Ribbon 工具的預設
* &amp;lbrack;內容&amp;rbrack;更新漸層建構資源以相容於 Ribbon

**修正**：

* &amp;lbrack;Crash&amp;rbrack;在啟用路徑吸附時載入另一個專案可能會當機
* &amp;lbrack;Crash&amp;rbrack;在 Path 面板中右鍵點擊，顯示剪貼簿中另一個工作階段的資訊，可能會當機
* &amp;lbrack;UI&amp;rbrack;介面在建立路徑時會在工具屬性中向上捲動
* &amp;lbrack;UI&amp;rbrack;當路徑視窗視覺化隱藏時，滑鼠游標會消失
* &amp;lbrack;Path&amp;rbrack;在路徑面板中複製貼上不同的工具屬性會導致不穩定的屬性
* &amp;lbrack;Tool&amp;rbrack;橡皮擦和污漬工具預設不一定會更新通道選擇
* &amp;lbrack;Tool&amp;rbrack;塗裝值為灰色，但 UI 在遮罩中載入彩色工具預設後顯示白色
* &amp;lbrack;Tool&amp;rbrack; 從遮罩建立的預設保留了從另一個預設載入的通道值
* &amp;lbrack;Substance&amp;rbrack;圖中定義的正常色彩空間覆寫不予考慮
* &amp;lbrack;Content&amp;rbrack; 預設筆刷形狀資源使用過時的物質

**已知問題**：

* 著色器實例歷史追蹤不當
* &amp;lbrack;Ribbon&amp;rbrack;UV磁磚的效能問題
* &amp;lbrack;Ribbon&amp;rbrack;路徑在某些情況下會在轉角後意外重疊
* &amp;lbrack;Ribbon&amp;rbrack;當點靠近路徑端點時，切線會產生不必要的迴圈
* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Ribbon&amp;rbrack; 在 Ribbon 中建立非常長的文字可能會當機
* &amp;lbrack;工具&amp;rbrack;材質預覽在遮罩中使用投影時無法運作
* &amp;lbrack;Baking&amp;rbrack;AO 設定「Self Occlusion」在多個材質集和啟用「以名稱匹配」時會被忽略
* &amp;lbrack;Baking&amp;rbrack;AO 搭配普通模式時，邊緣會有瑕疵，因為缺少填充
* &amp;lbrack;色彩管理&amp;rbrack;在 Linux 上使用 ACE 進行 HDR 色彩空間轉換會產生壓縮色彩
* &amp;lbrack;Regression&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 右鍵選單在 HD 螢幕上太小了
* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Python&amp;rbrack; USD export by TextureStateEvent 觸發
* &amp;lbrack;Engine&amp;rbrack;用克隆工具在正常通道色彩移位中繪製時，顏色移位錯誤
* &amp;lbrack;Python&amp;rbrack;Ghost 小工具似乎已被腳本刪除，但仍能運作

### 11.0.3

發行日期：**2025/08/05**&#x200B;摘要：**次要發行**

**補充**：

* &amp;lbrack;Substance 3D Assets&amp;rbrack;在 3D Assets 面板新增通知點
* &amp;lbrack;VFX Platform 2025&amp;rbrack; 在色彩管理設定中新增 ACES 2.0 設定
* &amp;lbrack;VFX 平台 2025&amp;rbrack;更新 OCIO 至 2.4.2 版本
* 更新 Iray 至 2024.10 版本
* &amp;lbrack;引擎&amp;rbrack;物質引擎 v.9.2.3 更新
* &amp;lbrack;Nvidia&amp;rbrack;將 Nvidia 驅動最低版本提升至 572.60（Win）和 570.169（Linux）

**修正**：

* &amp;lbrack;Python&amp;rbrack;範圍修改不會出現在歷史視窗中

**已知問題**：

* &amp;lbrack;色彩管理&amp;rbrack;在 Linux 上使用 ACE 進行 HDR 色彩空間轉換會產生壓縮色彩
* &amp;lbrack;Regression&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 右鍵選單在 HD 螢幕上太小了
* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Python&amp;rbrack; USD export by TextureStateEvent 觸發
* &amp;lbrack;Engine&amp;rbrack;用克隆工具在正常通道色彩移位中繪製時，顏色移位錯誤
* &amp;lbrack;Python&amp;rbrack;Ghost 小工具似乎已被腳本刪除，但仍能運作

### 11.0.2

發行日期：**2025/06/10**&#x200B;摘要：**次要發行**

**補充**：

* &amp;lbrack;Mac&amp;rbrack;新增警告，提醒特定作業系統版本會導致瑕疵
* &amp;lbrack;自動更新&amp;rbrack;資產錯誤日誌的輕微使用者體驗改進
* &amp;lbrack;自動展開&amp;rbrack;更新至版本 1.3.2，並改善接縫功能
* &amp;lbrack;USD&amp;rbrack;&amp;lbrack;FBX&amp;rbrack; 新增多重 UV 集合且資料稀疏的支援
* &amp;lbrack;Export&amp;rbrack;匯出為 FBX 的網格會缺少額外的 UV 集，如果匯入時有的話

**修正**：

* &amp;lbrack;MacOS&amp;rbrack;&amp;lbrack;Linux&amp;rbrack; 儲存在網路磁碟時當機
* &amp;lbrack;Win&amp;rbrack\lbrack;Tablet&amp;rbrack;平移時閃爍
* &amp;lbrack;SpaceMouse&amp;rbrack;使用路徑工具時的問題
* &amp;lbrack;自動籠子&amp;rbrack;網格重新載入後無法烘焙
* &amp;lbrack;自動更新&amp;rbrack;當缺少第一個圖塊時，影像序列不會重新載入
* &amp;lbrack;Path&amp;rbrack;自訂切線會影響其他切線
* &amp;lbrack;Path&amp;rbrack; 若第一個點位於另一個紋理集，則路徑不會出現在材質集上
* &amp;lbrack;UI&amp;rbrack;有些選單在開啟專案後總是會被禁用（例如：對稱）
* &amp;lbrack;Properties&amp;rbrack; 無法使用或載入填滿路徑工具的預設
* &amp;lbrack;USD&amp;rbrack;使用USD檔案時，自訂著色器無法辨識多個UV集合
* &amp;lbrack;USD&amp;rbrack;同名攝影機會被覆蓋
* &amp;lbrack;匯出&amp;rbrack;傳送到 Photoshop 結果會導致色彩空間不正確，無論是顏色還是灰階結果
* &amp;lbrack;Export&amp;rbrack;帶有 alpha 的灰階通道會以彩色匯出，而非帶有 PNG 格式的灰階
* &amp;lbrack;Export&amp;rbrack;將灰階通道匯出為 PSD 會導致檔案無效/截斷
* &amp;lbrack;內容&amp;rbrack;多向模式下的扭曲濾波器無法運作
* &amp;lbrack;Python&amp;rbrack;爬取層堆疊節點時無法配置列表錯誤

**已知問題**：

* &amp;lbrack;色彩管理&amp;rbrack;在 Linux 上使用 ACE 進行 HDR 色彩空間轉換會產生壓縮色彩
* &amp;lbrack;Regression&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 右鍵選單在 HD 螢幕上太小了
* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Python&amp;rbrack; USD export by TextureStateEvent 觸發
* &amp;lbrack;Engine&amp;rbrack;用克隆工具在正常通道色彩移位中繪製時，顏色移位錯誤
* &amp;lbrack;Python&amp;rbrack;Ghost 小工具似乎已被腳本刪除，但仍能運作

### 11.0.1

上映日期：**2025/04/10**&#x200B;摘要：**次要發行**

注意： **Linux CCD 版本將延後至 4 月 29 日**

**補充：**

* 更新至 Qt 6.5.8
* &amp;lbrack;Substance&amp;rbrack;當多個影像輸入共享相同用途時，新增過濾器日誌訊息
* &amp;lbrack;Nvidia&amp;rbrack;新增關於最新 Nvidia 驅動程式（572.47）的警告

**修正：**

* &amp;lbrack;Crash&amp;rbrack;拖放 SBSAR 且在單一通道槽中使用
* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Path&amp;rbrack; 在未點擊特定路徑時，變更路徑類型選項不會變成灰色。
* &amp;lbrack;填充路徑&amp;rbrack;不應能選擇物質材料
* &amp;lbrack;引擎與rbrack;沿筆觸的雜訊
* &amp;lbrack;引擎&amp;rbrack;路徑可以透過特定設定被斷開
* 滴管色域下拉選單的問題
* &amp;lbrack;Auto-update&amp;rbrack; &amp;lbrack;Python&amp;rbrack;使用 ResourceID 無版本時出現錯誤訊息
* &amp;lbrack;Shader&amp;rbrack;開啟某些專案時會崩潰

**已知問題：**

* &amp;lbrack;SpaceMouse&amp;rbrack;使用路徑工具時的問題
* &amp;lbrack;色彩管理&amp;rbrack;在 Linux 上使用 ACE 進行 HDR 色彩空間轉換會產生壓縮色彩
* &amp;lbrack;Regression&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 右鍵選單在 HD 螢幕上太小了
* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Python&amp;rbrack; USD export by TextureStateEvent 觸發
* &amp;lbrack;Engine&amp;rbrack;用克隆工具在正常通道色彩移位中繪製時，顏色移位錯誤
* &amp;lbrack;Python&amp;rbrack;Ghost 小工具似乎已被腳本刪除，但仍能運作

### 11.0.0

發行日期：**2025/03/11**&#x200B;摘要：**重大發行、新增自動更新功能、填補路徑工具及其他路徑改進，以及新篩選器與實驗性的自動籠式產生功能用於烘焙**

**補充**：

* 自動更新
* &amp;lbrack;自動更新&amp;rbrack;在資產面板中自動更新修改過的資產
* &amp;lbrack;自動更新&amp;rbrack;自動更新修改的資產
* &amp;lbrack;自動更新&amp;rbrack; 預設關閉自動更新
* &amp;lbrack;Auto-update&amp;rbrack;若資源參數不符（.sbsar、.glsl、.ai、.svg），則可選擇更新
* &amp;lbrack;Auto-update&amp;rbrack; 新增環境變數以停用自動更新功能
* &amp;lbrack;Auto-update&amp;rbrack;&amp;lbrack;SBSAR&amp;rbrack; 若資源參數不匹配，則將更新設為可選
* 填土路徑
* &amp;lbrack;Path&amp;rbrack;&amp;lbrack;Fill&amp;rbrack; 新增工具以建立填補路徑
* 步道改善
* &amp;lbrack;Path&amp;rbrack; 建立可吸附為多邊形的路徑
* &amp;lbrack;Path&amp;rbrack; 允許切換路徑類型
* &amp;lbrack;Path&amp;rbrack; 允許在內容與遮罩之間複製貼上路徑頂點資料
* &amp;lbrack;Path&amp;rbrack; 允許在建立新點時約束角度
* &amp;lbrack;Path&amp;rbrack; 允許對線建立限制點
* &amp;lbrack;Path&amp;rbrack;只需一鍵即可關閉形狀
* &amp;lbrack;Path&amp;rbrack; 顯示路徑資訊
* &amp;lbrack;Path&amp;rbrack; 允許縮放與旋轉路徑頂點
* &amp;lbrack;Path&amp;rbrack;&amp;lbrack;UX&amp;rbrack; 讓轉換工具更容易取得
* &amp;lbrack;Path&amp;rbrack; 新增路徑預覽
* &amp;lbrack;Path&amp;rbrack; 用 Shift + P 停用路徑預覽
* &amp;lbrack;Path&amp;rbrack; 從側面視圖改善切線版本
* &amp;lbrack;Path&amp;rbrack; 允許聚焦於三維路徑
* &amp;lbrack;Path&amp;rbrack;頂點在切換 UI 開關時應該會保留選取狀態
* &amp;lbrack;Path&amp;rbrack; 允許使用 Backspace 刪除路徑
* &amp;lbrack;Path&amp;rbrack; 如果使用者展開路徑列表，請保持開啟
* &amp;lbrack;Path&amp;rbrack;&amp;lbrack;Layer Stack&amp;rbrack; 正確地在複製/貼上時重命名重複的
* &amp;lbrack;Path&amp;rbrack;介面與提示改進
* 性能
* &amp;lbrack;Performance&amp;rbrack;在使用高鑲嵌層時提升視窗效能
* &amp;lbrack;Performance&amp;rbrack;在新的填充層/效果中只啟用第一個通道
* &amp;lbrack;Performance&amp;rbrack;筆觸計算平行化
* 烘焙
* &amp;lbrack;Baking&amp;rbrack; 新增全自動籠子生成選項，用於高多邊形網格烘焙（實驗性）
* 內容
* &amp;lbrack;Content&amp;rbrack; 新增 6 個濾鏡：樣式化、量化、各向異性桑原、斜角平滑、方向距離、灰階轉換
* &amp;lbrack;內容&amp;rbrack;將噪音與垃圾音樂更新至Designer最新版本（新增2D Voronoi）
* &amp;lbrack;內容&amp;rbrack;新增3個材質產生器（Tile Random、三角形格子、刮痕產生器）
* &amp;lbrack;內容&amp;rbrack;重新命名 Unreal Engine 範本與匯出預設
* Python
* &amp;lbrack;Shelf&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 從 Python 儲存智慧素材或智慧遮罩到磁碟
* &amp;lbrack;Python&amp;rbrack; Add baking auto-cage to Python API
* &amp;lbrack;Python&amp;rbrack; 允許編輯材質集/UV 圖塊名稱與描述
* &amp;lbrack;Python&amp;rbrack;分享向量與字型來源的解析度設定
* &amp;lbrack;Auto-update&amp;rbrack;&amp;lbrack;Python&amp;rbrack; Expose project auto-update functionsities in Python
* 其他
* &amp;lbrack;Export&amp;rbrack;讓新面板更容易存取「傳送到」選項
* &amp;lbrack;Nvidia&amp;rbrack;新增關於最新 Nvidia 驅動程式（572.16）的警告
* 角度吸附應該會受到物件/世界空間選擇的影響
* &amp;lbrack;貼圖集合列表&amp;rbrack;允許在 UV 圖塊中新增自訂名稱並在匯出時使用
* 麥克
* &amp;lbrack;Mac&amp;rbrack;圖形渲染時用 Metal 代替 OpenGL
* &amp;lbrack;Mac&amp;rbrack;取消 Mac Intel 支援

**修正**：

* &amp;lbrack;Crash&amp;rbrack; 刪除影像輸入
* 無法透過圖層堆疊按鈕新增智慧墊
* &amp;lbrack;Python&amp;rbrack;無法找到 GroupLayerNode 上的 Effects

**已知問題**：

* &amp;lbrack;色彩管理&amp;rbrack;在 Linux 上使用 ACE 進行 HDR 色彩空間轉換會產生壓縮色彩
* &amp;lbrack;Regression&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 右鍵選單在 HD 螢幕上太小了
* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Python&amp;rbrack; USD export by TextureStateEvent 觸發
* &amp;lbrack;MacOS Intel&amp;rbrack;匯入某些預設時會當機
* &amp;lbrack;Engine&amp;rbrack;用克隆工具在正常通道色彩移位中繪製時，顏色移位錯誤
* &amp;lbrack;Python&amp;rbrack;Ghost 小工具似乎已被腳本刪除，但仍能運作
* &amp;lbrack;RedHat&amp;rbrack;色彩選擇器問題

## 版本 10

### 10.1.2

發行日期：**2024/12/3**&#x200B;摘要：**小規模版本，修正錯誤**

**修正**：

* &amp;lbrack;Crash&amp;rbrack; 刪除影像輸入
* 無法透過圖層堆疊按鈕新增智慧墊
* &amp;lbrack;Python&amp;rbrack;無法找到 GroupLayerNode 上的 Effects

**已知問題**：

* &amp;lbrack;色彩管理&amp;rbrack;在 Linux 上使用 ACE 進行 HDR 色彩空間轉換會產生壓縮色彩
* &amp;lbrack;Regression&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 右鍵選單在 HD 螢幕上太小了
* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Python&amp;rbrack; USD export by TextureStateEvent 觸發
* &amp;lbrack;MacOS Intel&amp;rbrack;匯入某些預設時會當機
* &amp;lbrack;Engine&amp;rbrack;用克隆工具在正常通道色彩移位中繪製時，顏色移位錯誤
* &amp;lbrack;Python&amp;rbrack;Ghost 小工具似乎已被腳本刪除，但仍能運作
* &amp;lbrack;RedHat&amp;rbrack;色彩選擇器問題

### 10.1.1

發行日期：**2024/11/5**&#x200B;摘要：**小規模發行，修正錯誤**

**補充**：

* &amp;lbrack;Project&amp;rbrack; 保持目前專案開放，直到新專案選擇驗證完成
* &amp;lbrack;自動展開&amp;rbrack;Texel 密度允許更有效地將 UV 島嶼分割成 UDIM
* &amp;lbrack;Baking&amp;rbrack;修正網格地圖上下文選單中的歧義副本
* &amp;lbrack;Warp&amp;rbrack;移除視窗中 Z（深度）軸的縮放
* &amp;lbrack;匯入/匯出&amp;rbrack;移除未使用的影像檔案格式支援
* 更新 Substance Engine 至 9.1.4

**修正**：

* &amp;lbrack;崩潰&amp;rbrack;在資產資源轉移並節省專案後
* &amp;lbrack;Crash&amp;rbrack;aiserver 函式庫的問題
* &amp;lbrack;當機&amp;rbrack;Illustrator 伺服器在某些罕見情況下當機
* &amp;lbrack;Crash&amp;rbrack;在某些罕見情況下退出應用程式時
* 有些機器無法傳送當機報告
* &amp;lbrack;Baking&amp;rbrack;頂點顏色讀取不正確
* &amp;lbrack;UI&amp;rbrack;視窗的位置和啟動時的新內容被移位了
* &amp;lbrack;Assimp&amp;rbrack;Maya 的 StandardSurface 在 ID 烘焙中未被識別
* &amp;lbrack;Python&amp;rbrack; 缺少 SSL 函式庫會輸出錯誤
* &amp;lbrack;Python&amp;rbrack;&amp;lbrack;Win&amp;rbrack; 呼叫 QColorConstants.Transparent 時出錯
* &amp;lbrack;Python&amp;rbrack;圖層 用 Python 建立的縮圖在點擊圖層堆疊內部時不會重新整理
* &amp;lbrack;Shader&amp;rbrack; Shader API 變更日誌中的壞掉連結
* &amp;lbrack;3D 資產&amp;rbrack;存取 3D 資產時，請使用 OS 代理設定

**已知問題**：

* &amp;lbrack;色彩管理&amp;rbrack;在 Linux 上使用 ACE 進行 HDR 色彩空間轉換會產生壓縮色彩
* &amp;lbrack;Regression&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 在 HD 螢幕上右鍵選單太小
* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Python&amp;rbrack; USD export by TextureStateEvent 觸發
* &amp;lbrack;MacOS Intel&amp;rbrack;匯入某些預設時會當機
* &amp;lbrack;Engine&amp;rbrack;用克隆工具在正常通道色彩移位中繪製時，顏色移位錯誤
* &amp;lbrack;Python&amp;rbrack; 透過腳本似乎已刪除的小工具仍然有效
* &amp;lbrack;RedHat&amp;rbrack;色彩選擇器問題

### 10.1.0

發行日期：**2024/09/17**&#x200B;摘要：**重大版本，新增內容：填充區域遮罩/色彩濾鏡、刺繡貼紙濾鏡及六個通用 Substance 濾鏡，匯入含材質與著色器的 USD，效能提升，符合 2024 VFX 平台標準，並遷移至 Linux RedHat**

**補充**：

* &amp;lbrack;Content&amp;rbrack; 新增填充區域遮罩/色彩濾鏡
* &amp;lbrack;內容&amp;rbrack; 新增刺繡貼紙濾鏡
* &amp;lbrack;Content&amp;rbrack; 新增 6 個通用 Substance 濾波器（FXAA、像素化、高通、後置、平滑步進、閾值）
* &amp;lbrack;USD&amp;rbrack;輸出 USD 層，並定義 ASM 材料
* &amp;lbrack;USD&amp;rbrack;匯入 USD，並附帶材質與著色器屬性
* &amp;lbrack;Performance&amp;rbrack;預設啟用優化的圖層堆疊縮圖
* &amp;lbrack;Performance&amp;rbrack;減少專案檔案開啟時間與記憶體消耗（資料解碼）
* 符合 2024 年視覺特效平台標準
* &amp;lbrack;VFX 平台 2024&amp;rbrack;更新至 Python 3.11
* &amp;lbrack;VFX 平台 2024&amp;rbrack;OpenEXR 3.2 更新
* &amp;lbrack;VFX Platform 2024&amp;rbrack; &amp;lbrack;USD&amp;rbrack; Update OpenSubdiv 3.6.0
* &amp;lbrack;VFX 平台 2024&amp;rbrack;&amp;lbrack;色彩管理&amp;rbrack;更新至 OCIO 2.3.2
* &amp;lbrack;Linux&amp;rbrack; 遷移至 Linux RedHat
* &amp;lbrack;Linux&amp;rbrack;將 Nvidia 驅動程式的最小版本更新至 535.171.04
* &amp;lbrack;Import&amp;rbrack; 新增一個在匯入 GLTF 網格時翻轉法線貼圖的選項
* &amp;lbrack;UI&amp;rbrack; 使用作業系統預設值作為拖曳事件偵測距離
* &amp;lbrack;Substance Engine&amp;rbrack;新增呼叫條功能以移除可執行檔中的符號
* &amp;lbrack;啟動畫面&amp;rbrack;更新為新的啟動畫面格式
* 更新 Substance Engine 至 9.1.3 版本
* &amp;lbrack;Python&amp;rbrack;在圖層堆疊文件選單中顯示範例連結
* &amp;lbrack;JavaScript&amp;rbrack; 將 Javascript 外掛移至 javascript/plugins 子資料夾

**修正**：

* &amp;lbrack;Illustrator&amp;rbrack;在特定情況下匯出帶有 .ai 圖形的 UV 圖塊時當機
* &amp;lbrack;動態筆劃&amp;rbrack;&amp;lbrack;路徑&amp;rbrack;每筆劃隨機不會在路徑上運作
* &amp;lbrack;UI&amp;rbrack;&amp;lbrack;Properties&amp;rbrack; 當平鋪非均勻時會啟用鎖定
* 雙擊 Painter 專案時會建立除錯 TXT 檔案
* &amp;lbrack;USD&amp;rbrack;&amp;lbrack;Export&amp;rbrack;有些材質可能缺少
* &amp;lbrack;ASM&amp;rbrack;散射色彩通道忽略金屬色
* &amp;lbrack;內容&amp;rbrack;模糊濾鏡在「工作」色彩空間中無法運作
* &amp;lbrack;內容&amp;rbrack; 高度調整濾鏡也會修改圖層的 alpha 值

**已知問題**：

* &amp;lbrack;色彩管理&amp;rbrack;在 Linux 上使用 ACE 進行 HDR 色彩空間轉換會產生壓縮色彩
* &amp;lbrack;Win&amp;rbrack;&amp;lbrack;Crash&amp;rbrack; &amp;lbrack;ACE&amp;rbrack;顯示轉換時未使用 sRGB ICE 色彩空間
* &amp;lbrack;Regression&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 右鍵選單在 HD 螢幕上太小了
* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Python&amp;rbrack; USD export by TextureStateEvent 觸發
* &amp;lbrack;MacOS Intel&amp;rbrack;匯入某些預設時會當機
* &amp;lbrack;Crash&amp;rbrack;Relocate resource and save project
* &amp;lbrack;Engine&amp;rbrack;用克隆工具在正常通道色彩移位中繪製時，顏色移位錯誤
* &amp;lbrack;Python&amp;rbrack;Ghost 小工具似乎已被腳本刪除，但仍能運作
* &amp;lbrack;RedHat&amp;rbrack;色彩選擇器問題

### 10.0.1

發行日期： **2024/06/11**&#x200B;摘要： **小型釋出，修正錯誤**

**補充：**

* &amp;lbrack;Library&amp;rbrack; 將 Substance 字型轉換為一般字型檔案
* &amp;lbrack;Illustrator&amp;rbrack;&amp;lbrack;SVG&amp;rbrack; 在範圍選擇中，將縮圖設定為淺灰色背景
* &amp;lbrack;Python&amp;rbrack;在位圖來源上新增可用色彩空間的函式

**修正**：

* &amp;lbrack;疊加堆疊&amp;rbrack;資料夾在移動進出其他資料夾時總是關閉
* &amp;lbrack;Save&amp;rbrack;專案檔案在「另存為複製」或自動儲存失敗時會遺失
* &amp;lbrack;Import&amp;rbrack;同名但不同擴展名的資產會被覆蓋
* &amp;lbrack;Properties&amp;rbrack;在影像輸入中使用錨點時缺少設定
* &amp;lbrack;Illustrator&amp;rbrack;伺服器當機後無法匯入 Illustrator 檔案，除非重啟 Painter
* &amp;lbrack;Python&amp;rbrack;實例父節點不能用「properties」型別設定
* &amp;lbrack;Python&amp;rbrack;將高多邊形設為烘焙參數時，不會載入高多邊形
* &amp;lbrack;Python&amp;rbrack;set_color_space（） 的錯誤訊息過於通用
* &amp;lbrack;Python&amp;rbrack;參考來源允許建立循環

**已知問題**：

* &amp;lbrack;色彩管理&amp;rbrack;在 Linux 上使用 ACE 進行 HDR 色彩空間轉換會產生壓縮色彩
* &amp;lbrack;Regression&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 右鍵選單在 HD 螢幕上太小了
* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Python&amp;rbrack; USD export by TextureStateEvent 觸發
* &amp;lbrack;MacOS Intel&amp;rbrack;匯入某些預設時會當機
* &amp;lbrack;Illustrator&amp;rbrack;在特定情況下匯出帶有 .ai 圖形的 UV 圖塊時當機
* &amp;lbrack;動態筆劃&amp;rbrack;&amp;lbrack;路徑&amp;rbrack;每筆劃隨機不會在路徑上運作

### 10.0.0

發行日期： **2024/05/16**&#x200B;摘要： **重大版本，圖層堆疊版本與 Python API 同步，閱讀原生 Illustrator 檔案，整合 3D 資產與新文字資源**

**補充**：

* &amp;lbrack;Illustrator&amp;rbrack;在 Painter 中使用 Illustrator 檔案搭配藝術板
* &amp;lbrack;Illustrator&amp;rbrack;&amp;lbrack;SVG&amp;rbrack; Add previews in scope selection
* &amp;lbrack;Substance 3D 資產&amp;rbrack;直接在 Painter 中瀏覽、選擇並下載 3D 資產
* &amp;lbrack;Substance 3D 資產&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 新面板
* &amp;lbrack;Substance 3D 資產&amp;rbrack;支援環境地圖與材質
* &amp;lbrack;Substance 3D 資產&amp;rbrack;允許重新載入、導航及在新的 Substance 3D 資產面板中開啟位置資料夾
* &amp;lbrack;Substance 3D 資產&amp;rbrack;新增下載管理器
* &amp;lbrack;Text Resource&amp;rbrack;允許使用可嵌入字型
* &amp;lbrack;Text Resource&amp;rbrack; 允許在網格上渲染字型/文字
* &amp;lbrack;Text Resource&amp;rbrack;在資產面板中顯示使用者及其他共享路徑的字型，並新增類別
* &amp;lbrack;Text Resource&amp;rbrack;&amp;lbrack;Properties&amp;rbrack; 新增對進階字型屬性的支援
* &amp;lbrack;Text Resource&amp;rbrack;允許在迷你書架中搜尋/檢視字型
* &amp;lbrack;Text Resource&amp;rbrack; 匯入不相容字型時新增錯誤訊息/對話框
* 其他
* &amp;lbrack;填充投影&amp;rbrack;改善使用小值時尺度操作器的行為
* &amp;lbrack;Manipulators&amp;rbrack;按 CTRL 捷徑時新增精確模式
* &amp;lbrack;操作手&amp;rbrack;提升平面操作手在平移時的穩定性
* &amp;lbrack;Export&amp;rbrack;在 SBSAR 輸出中新增色彩空間名稱
* &amp;lbrack;Performance&amp;rbrack;提升磁碟上資產的資料庫發現時間
* &amp;lbrack;Substance&amp;rbrack;Substance 引擎版本 9.1.2 更新
* &amp;lbrack;拖曳並下放&amp;rbrack;在視窗中放置貼紙時，將貼紙旋轉對準攝影機
* &amp;lbrack;Python&amp;rbrack; 層疊版本
* &amp;lbrack;Python&amp;rbrack;允許在 UI 中選擇圖層、效果、遮罩、幾何遮罩
* &amp;lbrack;Python&amp;rbrack; 允許取得/設定圖層混合模式
* &amp;lbrack;Python&amp;rbrack; 允許取得/設定填充層投影設定
* &amp;lbrack;Python&amp;rbrack; 允許從填充層查詢 Substance 材質顏色
* &amp;lbrack;Python&amp;rbrack;允許查詢並設定圖層與效果中的統一顏色與資源
* &amp;lbrack;Python&amp;rbrack;允許在圖層堆疊中建立與編輯文字資源
* &amp;lbrack;Python&amp;rbrack;允許編輯圖層與效果上的主動通道
* &amp;lbrack;Python&amp;rbrack;允許批次動作進行單一的復原/重做
* &amp;lbrack;Python&amp;rbrack; 允許載入/編輯向量來源參數
* &amp;lbrack;Python&amp;rbrack;允許透過色彩管理編輯圖層及效果色彩屬性
* &amp;lbrack;Python&amp;rbrack; 允許查詢並建立實例化圖層
* &amp;lbrack;Python&amp;rbrack; 允許加入顏色選擇效果
* &amp;lbrack;Python&amp;rbrack; 允許控制點陣圖影像色彩管理
* &amp;lbrack;Python&amp;rbrack; 允許暫停/解除暫停引擎
* &amp;lbrack;Python&amp;rbrack; 允許導覽至兄弟節點與父節點
* &amp;lbrack;Python&amp;rbrack;允許建立濾波器/產生器效果
* &amp;lbrack;Python&amp;rbrack; 允許加入音量效果
* &amp;lbrack;Python&amp;rbrack; 允許在圖層上新增智慧遮罩
* &amp;lbrack;Python&amp;rbrack; 允許建立/編輯錨點
* &amp;lbrack;Python&amp;rbrack; 允許在圖層上取得/設定遮罩
* &amp;lbrack;Python&amp;rbrack; 允許建立比較遮罩效果
* &amp;lbrack;Python&amp;rbrack;允許查詢並使用 Substance 資源中的預設
* &amp;lbrack;Python&amp;rbrack;允許透過 Substance 資源的預設值列表 internal_properties 函式
* &amp;lbrack;Python&amp;rbrack; 允許列出預設的匯出預設預設
* &amp;lbrack;Python&amp;rbrack;允許列出函式庫中可用的匯出預設
* &amp;lbrack;Python&amp;rbrack; 允許擷取匯出預設的內容

**修正**：

* &amp;lbrack;Crash&amp;rbrack; 用 Ctrl-Z 還原「移除著色器實例」
* &amp;lbrack;Crash&amp;rbrack; 如果最後選擇是效果，則在空堆疊上建立圖層
* &amp;lbrack;SVG&amp;rbrack;自訂裁切區域值的問題
* &amp;lbrack;自動展開&amp;rbrack;僅重新計算包裝且不改變 UV 方向，會導致當機
* &amp;lbrack;拖放&amp;rbrack;外部資源延遲會多次預先載入
* &amp;lbrack;UI&amp;rbrack;拖放資源縮圖可以在圖層堆疊中隱藏警告訊息
* &amp;lbrack;Performance&amp;rbrack;遮蔽 UV 圖塊仍會被計算
* &amp;lbrack;USD&amp;rbrack;範圍選擇的標示錯誤
* &amp;lbrack;Resource&amp;rbrack;點陣圖影像在正常通道繪製並儲存專案後會損壞
* &amp;lbrack;USD&amp;rbrack;支援左手頂點網格排序
* &amp;lbrack;Substance&amp;rbrack; 重設為預設，角度小工具總是回到零
* &amp;lbrack;Engine&amp;rbrack;用 SVG 在模板上繪製是不行的
* &amp;lbrack;Engine&amp;rbrack;法線貼圖筆觸在復原後會中斷
* &amp;lbrack;內容&amp;rbrack;圖形轉材質濾鏡的 alpha 混合和色彩空間不正確
* &amp;lbrack;內容&amp;rbrack;圖塊產生器的混合模式無法運作
* &amp;lbrack;Content&amp;rbrack;直方圖掃描濾波器在某些情況下會產生條紋
* &amp;lbrack;內容&amp;rbrack;風格化的烘焙光影不考慮繪畫高度
* &amp;lbrack;Python&amp;rbrack;著色器更換後取得實例層資訊時出現意外錯誤
* &amp;lbrack;Save&amp;rbrack;專案檔案在特定情況下「另存為」失敗時會遺失

**已知問題**：

* &amp;lbrack;色彩管理&amp;rbrack;在 Linux 上使用 ACE 進行 HDR 色彩空間轉換會產生壓縮色彩
* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Linux&amp;rbrack;&amp;lbrack;AMD&amp;rbrack; 在 Wayland OS 的層堆疊中拖放資源
* &amp;lbrack;Regression&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 在 HD 螢幕上右鍵選單太小了
* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Python&amp;rbrack; USD export by TextureStateEvent 觸發
* &amp;lbrack;Save&amp;rbrack;Spp 專案檔案在特定情況下「另存為複製」失敗時會遺失
* &amp;lbrack;MacOS Intel&amp;rbrack;匯入某些預設時會當機
* &amp;lbrack;Illustrator&amp;rbrack;伺服器當機後無法匯入 AI 檔案，除非重啟 Painter
* &amp;lbrack;Import&amp;rbrack;同名但不同擴展名的資產會被覆蓋

## 版本9

### 9.1.2

發行日期：**2024/01/30**&#x200B;摘要：**小規模釋出，修正錯誤**

**補充**：

* &amp;lbrack;Performance&amp;rbrack;改善新專案的首次填充層建立時間
* &amp;lbrack;Performance&amp;rbrack;減少重度環境貼圖的載入時間
* &amp;lbrack;Substance&amp;rbrack;允許在產生縮圖時儲存/關閉專案

**修正**：

* 在修改視窗時，舊版本專案的存檔會失敗
* &amp;lbrack;Crash&amp;rbrack;使用自訂 AO 和色彩管理時重新匯入網格
* &amp;lbrack;填充投影&amp;rbrack;點擊比例操控器會顯示「無法繪製」訊息
* &amp;lbrack;Brush&amp;rbrack;用 UV 對齊的繪畫會產生瑕疵
* &amp;lbrack;層疊&amp;rbrack;當堆疊非常長時，層名重命名會很慢
* &amp;lbrack;Layer Stack&amp;rbrack;在遮罩中使用不相容濾波器時出現錯誤訊息
* &amp;lbrack;Layer stack&amp;rbrack;刪除後選擇會切回頂層
* &amp;lbrack;Export&amp;rbrack;產生的法線貼圖總是處於 3D 空間鄰居填充模式
* &amp;lbrack;Export&amp;rbrack;紋理 alpha 並非使用 2D View 匯出預設產生
* &amp;lbrack;Export&amp;rbrack;SBSAR export 在轉換後的地圖使用方式不正確
* &amp;lbrack;Shader&amp;rbrack;Shader API 變更日誌尚未更新，尚未更新最新的 ASM 變更

**已知問題**：

* &amp;lbrack;色彩管理&amp;rbrack;在 Linux 上使用 ACE 進行 HDR 色彩空間轉換會產生壓縮色彩
* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Linux&amp;rbrack;&amp;lbrack;AMD&amp;rbrack; 在 Wayland OS 的層堆疊中拖放資源
* &amp;lbrack;Regression&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 在 HD 螢幕上右鍵選單太小了
* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Python&amp;rbrack; USD export by TextureStateEvent 觸發

### 9.1.1

發行日期：**2023/12/05**&#x200B;摘要：**小規模版本、錯誤修正及傳送到 After Effects 功能**

**補充：**

* &amp;lbrack;Interop&amp;rbrack;允許將貼圖網格傳送至 After Effects（Ae 24.1）

**修正：**

* &amp;lbrack;Fill&amp;rbrack; UV 設定為 UV 集合投影時，不會讀取超過 2 組 UV 集合
* &amp;lbrack;Crash&amp;rbrack;使用 16K 環境地圖
* &amp;lbrack;Crash&amp;rbrack;Exr 用作影像輸入
* &amp;lbrack;Crash&amp;rbrack;跨專案複製貼上路徑
* &amp;lbrack;QoL&amp;rbrack;在貼花模式下拖放 Alpha 資源，會在遮罩中產生 UV 投影
* &amp;lbrack;Path&amp;rbrack;複製路徑頂點時，重新開啟專案時也會重新命名目標路徑
* &amp;lbrack;Linux&amp;rbrack;色彩選擇可以在多個畫面中被破壞
* &amp;lbrack;自動展開&amp;rbrack;用於像素密度控制的 UI 問題
* &amp;lbrack;色彩管理&amp;rbrack;UI 回饋是合理的，但引擎卻不行
* &amp;lbrack;色彩管理&amp;rbrack;遮罩中使用者資料覆蓋時色彩空間選擇錯誤

**已知問題：**

* &amp;lbrack;色彩管理&amp;rbrack;在 Linux 上使用 ACE 進行 HDR 色彩空間轉換會產生壓縮色彩
* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Linux&amp;rbrack;在 AMD 上拖放資源時，使用 Linux Wayland 在 Layer Stack 中
* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Mac&amp;rbrack; 在 Monterey OS 上更改各向異性過濾值
* &amp;lbrack;Regression&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 右鍵選單在 HD 螢幕上太小了
* &amp;lbrack;Python&amp;rbrack; TexStateEvent 觸發的 Crash 匯出 USD

### 9.1.0

發行日期： **2023/11/07**&#x200B;摘要： **重大版本引入 SVG 與透明度支援，以及拖放與路徑工具的改進**

**補充：**

* &amp;lbrack;SVG&amp;rbrack; 允許匯入向量檔案（SVG）
* &amp;lbrack;SVG&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 新增對 SVG 專屬屬性的支援
* &amp;lbrack;SVG&amp;rbrack; 新增選項以輕鬆保留原始影像比例
* &amp;lbrack;SVG&amp;rbrack; 允許自動使用 SVG 的透明度 alpha
* &amp;lbrack;Interop&amp;rbrack;允許將貼圖網格傳送至 After Effects（AE 24.1 beta）
* &amp;lbrack;Interop&amp;rbrack; 新增傳送到 After Effects 的設定
* &amp;lbrack;QoL&amp;rbrack;&amp;lbrack;Assets&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 拖放到 UI 欄位時自動匯入資產
* &amp;lbrack;QoL&amp;rbrack;允許將外部資產拖放到圖層堆疊中
* &amp;lbrack;QoL&amp;rbrack;&amp;lbrack;圖層堆疊&amp;rbrack;將材質從資產面板拖放到圖層堆疊中
* &amp;lbrack;QoL&amp;rbrack;&amp;lbrack;Viewport&amp;rbrack; 允許拖放產生器，網格上的過濾器
* &amp;lbrack;QoL&amp;rbrack;&amp;lbrack;Viewport&amp;rbrack; 允許將外部資產丟入網狀網路
* &amp;lbrack;QoL&amp;rbrack;&amp;lbrack;Projection&amp;rbrack; 新增 UV 設定為 UV 設定投影模式
* &amp;lbrack;QoL&amp;rbrack;將智慧口罩拖放為視窗與圖層堆疊中的新圖層
* &amp;lbrack;QoL&amp;rbrack;在遮罩中使用時，為多輸出產生器新增選擇器
* &amp;lbrack;QoL&amp;rbrack;允許拖放單一通道影像於填充效果上
* &amp;lbrack;QoL&amp;rbrack;&amp;lbrack;Layer stack&amp;rbrack; 使用 CTRL/ALT 修飾鍵搭配拖放，指定在哪裡/如何建立效果/圖層
* &amp;lbrack;Path&amp;rbrack;在路徑面板中分別切換路徑可見性
* &amp;lbrack;Path&amp;rbrack; 允許使用轉換操作器來管理路徑點
* &amp;lbrack;Path&amp;rbrack; 允許手動控制每個頂點的切線
* &amp;lbrack;Path&amp;rbrack; 複製/貼上路徑屬性
* &amp;lbrack;Path&amp;rbrack; 引入一個空的切線按鈕快捷鍵
* &amp;lbrack;Shader&amp;rbrack;在 ASM shader 中新增對不透明度與半透明性的支援
* &amp;lbrack;Shader&amp;rbrack;新增 ASM 著色器對吸收色彩通道的支援
* &amp;lbrack;Shader&amp;rbrack;改進 ASM 著色器參數工具提示
* &amp;lbrack;Shader&amp;rbrack;將半透明通道預設顏色改為黑色
* &amp;lbrack;顯示設定&amp;rbrack;預設啟用時間抗鋸齒
* &amp;lbrack;顯示設定&amp;rbrack;預設啟用次表面散射設定
* &amp;lbrack;Substance&amp;rbrack;新增對圖形輸入/輸出 ColorSpace 屬性的支援
* &amp;lbrack;Substance&amp;rbrack;將Substance引擎更新至9.0.3版本
* &amp;lbrack;UI&amp;rbrack; 即使應用程式視窗很小，也讓上下文工具列按鈕可存取
* &amp;lbrack;自動展開&amp;rbrack;控制 UV 磚塊數與 Texel 密度
* &amp;lbrack;Baking&amp;rbrack;預設情況下停用 AMD GPU 的光線追蹤
* &amp;lbrack;Performance&amp;rbrack;對 16 位元影像應用無損壓縮以減少專案佔用空間
* &amp;lbrack;Python&amp;rbrack; 允許在 3D 視圖中操作預設攝影機
* &amp;lbrack;Python&amp;rbrack;透過腳本揭露匯出網格的能力
* &amp;lbrack;內容&amp;rbrack;&amp;lbrack;Samples&amp;rbrack; 新增範例專案「法國餐廳餐桌」
* &amp;lbrack;內容&amp;rbrack;更新Substance標誌alpha至新版本
* &amp;lbrack;內容&amp;rbrack;新增三個以 SVG 為核心的材質過濾器（自訂貼紙、自訂噴塗與材質圖像）

**修正：**

* &amp;lbrack;Crash&amp;rbrack; 在不使用對稱工具時改變操作手大小
* &amp;lbrack;Crash&amp;rbrack; &amp;lbrack;Layer stack&amp;rbrack;當沒有選擇時建立圖層
* &amp;lbrack;Project&amp;rbrack;網格貼圖在移除未使用資源後可能會損壞
* &amp;lbrack;Project&amp;rbrack;重新匯入或重新烘焙映像後的資源損毀
* &amp;lbrack;資產&amp;rbrack;重新載入資產會將其從收藏夾移除
* &amp;lbrack;Import&amp;rbrack;當資產面板顯示「找不到結果」時，無法匯入資源
* &amp;lbrack;UI&amp;rbrack;情境工具列箭頭在某些情況下不會出現
* &amp;lbrack;Substance&amp;rbrack;不支援布林值的並排按鈕
* &amp;lbrack;Level&amp;rbrack;遮罩使用時通道標籤錯誤
* &amp;lbrack;Export&amp;rbrack;&amp;lbrack;glTF&amp;rbrack; 從 Painter 匯出的 glTF/GLB 檔案沒有實體大小單位
* &amp;lbrack;內容&amp;rbrack;模糊濾波器強度被壓縮為16
* &amp;lbrack;內容&amp;rbrack;色彩匹配濾鏡「目標顏色」影像輸入不可見

**已知問題：**

* &amp;lbrack;色彩管理&amp;rbrack;在 Linux 上使用 ACE 進行 HDR 色彩空間轉換會產生壓縮色彩
* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Linux&amp;rbrack;在 AMD 上拖放資源時，使用 Linux Wayland 在 Layer Stack 中
* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Mac&amp;rbrack; 在 Monterey OS 上更改各向異性過濾值
* &amp;lbrack;Crash&amp;rbrack;Exr 用作影像輸入
* &amp;lbrack;Crash&amp;rbrack;使用 16K 環境地圖
* &amp;lbrack;自動展開&amp;rbrack;用於像素密度控制的 UI 問題
* &amp;lbrack;Regression&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 右鍵選單在 HD 螢幕上太小了
* &amp;lbrack;Python&amp;rbrack; TexStateEvent 觸發的 Crash 匯出 USD
* &amp;lbrack;QoL&amp;rbrack;在貼花模式下拖放 Alpha 資源，會在遮罩中產生 UV 投影

### 9.0.1

發行日期： **2023/09/19**&#x200B;摘要： **小規模錯誤修正釋出，並附有多項改進**

**補充：**

* &amp;lbrack;Import&amp;rbrack; 在匯入視窗中設定預設匯入位置
* &amp;lbrack;烘焙模式&amp;rbrack;允許將參數重設為預設值
* &amp;lbrack;Baking&amp;rbrack; 在建立專案時，將烘焙設定為繪畫解析度
* &amp;lbrack;對稱&amp;rbrack;從快捷鍵Q中解開對稱特定操作器的束縛
* &amp;lbrack;Menu&amp;rbrack; 在說明選單中新增「顯示日誌」選項
* &amp;lbrack;Viewport&amp;rbrack; 提升陰影渲染速度
* &amp;lbrack;Substance&amp;rbrack;引擎更新至版本 9.0.1
* &amp;lbrack;色彩管理&amp;rbrack;OCIO 設定檔可以有任何副檔名類型
* &amp;lbrack;Assets&amp;rbrack;帶有「貼花」使用量的 Sbsar 資源應該自動設定為曲速投影
* &amp;lbrack;Path&amp;rbrack;當 UI 和 Gizmos 隱藏時，嘗試與 Path 工具互動時會顯示訊息

**修正：**

* &amp;lbrack;撞擊&amp;rbrack;Alt + 拖曳路徑面板
* &amp;lbrack;匯入資源&amp;rbrack;移除資源匯入時隨機崩潰
* 匯入壓縮後的 GLB 檔案時會當機
* 在共用 UV 的網格上色時出現的問題
* 重新計算或載入快取時，網格閃爍黑色
* &amp;lbrack;Properties&amp;rbrack;右鍵選單重置參數不會出現在下拉選單中
* &amp;lbrack;Level&amp;rbrack;輸入滑桿依前一關鎖定
* &amp;lbrack;AMD&amp;rbrack;&amp;lbrack;Sparse&amp;rbrack;啟用時 SVT 選項會產生雜訊
* &amp;lbrack;投影&amp;rbrack;&amp;lbrack;Warp&amp;rbrack;雙擊頂點時崩潰
* &amp;lbrack;Path&amp;rbrack;烘焙模式下可見的 UI 與路徑
* &amp;lbrack;AMD&amp;rbrack;調整可見度時紋理會遺失
* &amp;lbrack;Sparse&amp;rbrack;轉動網格時解析度太低

**已知問題：**

* &amp;lbrack;色彩管理&amp;rbrack;在 Linux 上使用 ACE 進行 HDR 色彩空間轉換會產生壓縮色彩

### 9.0.0

發行日期：**2023/06/20**&#x200B;摘要：**重大發行，沿路徑 Paint 支援 3D 曲線、新基底材質、清理舊材質及 3D 曲線新預設**

**補充：**

* &amp;lbrack;Path&amp;rbrack; 新增沿路徑繪圖工具
* &amp;lbrack;Path&amp;rbrack; 為路徑工具新增一個空的捷徑
* &amp;lbrack;Path&amp;rbrack; 允許在現有路徑上新增點
* &amp;lbrack;Path&amp;rbrack; 新增捷徑以退出目前的路徑建立
* &amp;lbrack;Path&amp;rbrack; 允許編輯路徑的刷子屬性
* &amp;lbrack;Path&amp;rbrack;放置點時自動調整切線
* &amp;lbrack;Path&amp;rbrack;在點移動時重新計算切線
* &amp;lbrack;Path&amp;rbrack; 新建立的 Snap 指向網格表面
* &amp;lbrack;Path&amp;rbrack; 允許編輯每個頂點的壓力
* &amp;lbrack;Path&amp;rbrack; 調整鄰近點新建立點的壓力
* &amp;lbrack;Path&amp;rbrack;允許將點轉換為平滑/角角（切線斷開）
* &amp;lbrack;Path&amp;rbrack; 允許立即移動新加入的點
* &amp;lbrack;Path&amp;rbrack; 允許從現有路徑中移除點
* &amp;lbrack;Path&amp;rbrack; 允許反轉路徑的方向
* &amp;lbrack;Path&amp;rbrack; 允許在視窗中選擇路徑
* &amp;lbrack;Path&amp;rbrack; 允許透過標記選取路徑點
* &amp;lbrack;Path&amp;rbrack; 引入 CTRL-A 捷徑，可選取路徑上的所有點
* &amp;lbrack;Path&amp;rbrack; 允許關閉路徑
* &amp;lbrack;Path&amp;rbrack; 允許在屬性中指定路徑上方軸
* &amp;lbrack;Path&amp;rbrack; 在上下文工具列新增頂點控制選單
* &amp;lbrack;Path&amp;rbrack;在路徑工具中引入繪圖/擦除/污漬模式
* &amp;lbrack;Path&amp;rbrack; 為視窗中的路徑建立視覺回饋
* &amp;lbrack;Path&amp;rbrack;新增路徑方向的視覺指示器
* &amp;lbrack;Path&amp;rbrack; 在路徑顯示設定中加入線條粗細
* &amp;lbrack;Path&amp;rbrack; 允許隱藏路徑 UI
* &amp;lbrack;Path&amp;rbrack; 新增路徑面板以列出目前選取圖層的路徑
* &amp;lbrack;Path&amp;rbrack; 在路徑面板中滑鼠移至路徑時，新增視覺回饋
* &amp;lbrack;Path&amp;rbrack;當選擇路徑工具時，顯示路徑面板
* &amp;lbrack;Path&amp;rbrack; 允許在路徑面板中重新命名、刪除、複製、剪切及複製路徑
* &amp;lbrack;Path&amp;rbrack;嘗試在 2D 視口中使用 Path 工具互動時顯示訊息
* &amp;lbrack;Library&amp;rbrack;整合新內容（路徑工具與基礎資料）
* &amp;lbrack;動態筆劃&amp;rbrack; 為動態筆劃新增距離屬性
* &amp;lbrack;動態筆劃&amp;rbrack; 為動態筆劃添加大小與間距屬性
* &amp;lbrack;動態筆劃&amp;rbrack; 新增動態筆劃的起始/中間/結尾屬性
* &amp;lbrack;Python&amp;rbrack;&amp;lbrack;USD&amp;rbrack; Expose project configuration parameters for the USD 格式
* &amp;lbrack;Python&amp;rbrack;&amp;lbrack;USD&amp;rbrack; Expose 項目創建參數以 USD 格式
* &amp;lbrack;Export&amp;rbrack;&amp;lbrack;USD&amp;rbrack; 在匯出的美元檔案中新增專案路徑資訊
* &amp;lbrack;GLTF&amp;rbrack;重新載入 GLTF 檔案時，更新函式庫中的材質
* &amp;lbrack;Shader&amp;rbrack;減少不同方向UV島的接縫偽影
* &amp;lbrack;Engine&amp;rbrack;Substance 引擎版本 9.0 更新

**修正：**

* &amp;lbrack;Import&amp;rbrack;有些帶有貼圖的 GLB 在 Painter 中無法取得貼圖
* &amp;lbrack;AMD&amp;rbrack;所有3D投影填充邊框上的雜訊
* &amp;lbrack;Engine&amp;rbrack;切換圖層可見性時貼圖會中斷
* &amp;lbrack;Engine&amp;rbrack;切換混合模式時，有些地方的貼圖是空白的
* &amp;lbrack;Engine&amp;rbrack;紋理/投影在某些情況下是空的曲速模式
* &amp;lbrack;Iray&amp;rbrack;儲存渲染時，迭代重置為 0
* &amp;lbrack;Log&amp;rbrack;執行檔案>新檔時的USD錯誤訊息

**已知問題：**

* &amp;lbrack;色彩管理&amp;rbrack;在 Linux 上使用 ACE 進行 HDR 色彩空間轉換會產生壓縮色彩
* &amp;lbrack;層疊疊&amp;rbrack;輸入來源不會在每層儲存

## 版本8

### 8.3.1

上映日期： **2023/04/27**

**補充：**

* &amp;lbrack;Baking Mode&amp;rbrack; 新增（空）捷徑以顯示或隱藏視窗視覺化
* &amp;lbrack;烘焙模式&amp;rbrack;使用「隱藏烘焙網格」按鈕時，總是顯示低多邊形
* &amp;lbrack;烘焙模式&amp;rbrack;根據目前材質集顯示名稱匹配後綴
* &amp;lbrack;Import&amp;rbrack; 新增對 GLTF 二進位檔案（glb）的支援
* &amp;lbrack;紋理集合列表&amp;rbrack; 新增選單以選取或建立著色器實例
* &amp;lbrack;貼圖集列表&amp;rbrack;允許快速更改貼圖集與 UV 圖塊解析度
* &amp;lbrack;物理尺寸&amp;rbrack;在使用物理尺寸進行紫外線投影時，改善操作手的行為
* &amp;lbrack;UI&amp;rbrack;將「另存為」重新啟用至主檔案選單
* &amp;lbrack;UI&amp;rbrack;在 UI 佈局中儲存視圖選擇（僅 2D、僅 3D，兩者皆有）
* &amp;lbrack;USD&amp;rbrack;專案建立時不支援美元的錯誤訊息較不模糊
* &amp;lbrack;Python&amp;rbrack; 新增烘焙事件以追蹤烘焙進度
* &amp;lbrack;Python&amp;rbrack; 允許取消烘焙
* &amp;lbrack;Python&amp;rbrack;在匯出時，揭露「基於輸出範本」的檔案類型與位深
* &amp;lbrack;Python&amp;rbrack; Expose refresh time for TextureStateEvent.Update

**修正：**

* &amp;lbrack;Crash&amp;rbrack;專案結束時罕見的崩潰
* &amp;lbrack;Crash&amp;rbrack; &amp;lbrack;Baking&amp;rbrack; 啟用網格貼圖與特定專案的高度或曲率同步
* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Scripting&amp;rbrack; 在著色器實例建立後新增材質時會崩潰
* &amp;lbrack;烘烤模式&amp;rbrack;中性材料中的AO強度不影響
* &amp;lbrack;烘焙模式&amp;rbrack;在模型載入前切換到烘焙模式時會當機
* &amp;lbrack;烘焙模式&amp;rbrack;烘焙過程標籤中缺少錯誤訊息
* &amp;lbrack;烘焙模式&amp;rbrack;中性材質設定在重新匯入網格後不會有影響
* &amp;lbrack;烘焙模式&amp;rbrack;視窗分隔器會全域儲存，而非每個模式
* &amp;lbrack;烘焙模式&amp;rbrack;視覺化問題：平均法線不會改變籠子表面
* &amp;lbrack;色彩管理&amp;rbrack;當 OCIO 環境變數存在時，自動偵測色彩空間設定會被停用
* &amp;lbrack;Content&amp;rbrack; 遮罩輪廓濾波器有帶有高度輸入的雜訊
* &amp;lbrack;內容&amp;rbrack;斜率模糊濾鏡強度滑桿被夾在 1.0
* &amp;lbrack;Interop&amp;rbrack;無法在 Sampler 中使用 GLTF 建立專案
* &amp;lbrack;Layer Stack&amp;rbrack;投影平鋪值未正確更新於操作器中
* &amp;lbrack;Linux&amp;rbrack;HDPI 超過 100% 時，繪圖板筆與游標之間的偏移
* &amp;lbrack;Python&amp;rbrack;在建立專案後重新匯入網格時會當機
* &amp;lbrack;Substance&amp;rbrack;重新匯入網格後，3D 噪音會被破壞
* &amp;lbrack;UV 磁磚&amp;rbrack;UV投影的偏移被夾在1
* &amp;lbrack;視窗&amp;rbrack;直線的視覺回饋不再可見
* &amp;lbrack;WhatsNew&amp;rbrack;特色標題回傳行錯

**已知問題：**

* &amp;lbrack;Import&amp;rbrack;有些帶有貼圖的 GLB 在 Painter 中無法取得貼圖

### 8.3.0

*（發布日期：2023* 年 1 月 10 日）摘要： **重大版本，新增烘焙模式、新的 USD 檔案匯入與匯出功能，以及 UV 投影的實體尺寸支援**

**補充：**

* &amp;lbrack;烘焙模式&amp;rbrack;全新專為烘焙過程設計的烘焙模式

* &amp;lbrack;烘焙模式&amp;rbrack;將切換到烘焙模式的快捷鍵設為 F8

* &amp;lbrack;烘焙模式&amp;rbrack;在視窗中新增開始與取消烘焙按鈕

* &amp;lbrack;烘焙模式&amp;rbrack;在材質集合列表中新增烘焙選擇

* &amp;lbrack;烘焙模式&amp;rbrack; 新增網格地圖烘焙視窗以選取烘焙者

* &amp;lbrack;烘焙模式&amp;rbrack; 新增網格貼圖設定視窗以編輯烘焙設定

* &amp;lbrack;烘焙模式&amp;rbrack; 新增烘焙日誌視窗以追蹤烘焙過程

* &amp;lbrack;烘焙模式&amp;rbrack;將烘焙參數及復原動作加入歷史視窗

* &amp;lbrack;烘焙模式&amp;rbrack; 在網格地圖設定中加入麵包屑

* &amp;lbrack;烘焙模式&amp;rbrack; 在 Mesh Map Bakers 視窗中新增網格貼圖縮圖

* &amp;lbrack;烘焙模式&amp;rbrack;在3D視窗中新增可摺疊選單的視覺化設定

* &amp;lbrack;烘焙模式&amp;rbrack;新增視覺化設定以顯示/隱藏高多邊形網格

* &amp;lbrack;烘焙模式&amp;rbrack; 新增視覺化設定以顯示/隱藏籠子網格與線框

* &amp;lbrack;烘焙模式&amp;rbrack; 新增可視化設定以顯示或隱藏低多邊形網格

* &amp;lbrack;烘焙模式&amp;rbrack;新增視覺化設定，顯示沒有 UV 接縫的硬邊錯誤

* &amp;lbrack;烘焙模式&amp;rbrack;若烘焙日誌未顯示，請在視窗中告知網格與烘焙錯誤

* &amp;lbrack;烘焙模式&amp;rbrack;新增動作以同步所有材質集的烘焙設定

  在 Mesh Map Bakers 視窗中，每個烘焙者（以及共用設定）都可以點擊其名稱旁的連結圖示來同步。 這個動作會開啟一個視窗，讓你選擇哪些材質集會共享相同參數。

* &amp;lbrack;烘焙模式&amp;rbrack; 新增複製貼上烘焙設定的動作

  在網格貼圖 Bakers 視窗中，可以透過視窗頂端的專用選單或右鍵上下文選單，將每個烘焙者設定複製並貼上到貼圖集各處。

* &amp;lbrack;烘焙模式&amp;rbrack;在烘焙日誌中新增按鈕，從錯誤跳到正確設定

  當烘焙機失敗或網格無法正常載入時，烘焙日誌會出現錯誤訊息。 訊息旁邊的按鈕可以切換網格地圖烘焙器和網格地圖設定視窗，顯示相關設定。 這有助於更容易找出問題根源，進而修復。

* &amp;lbrack;烘焙模式&amp;rbrack;新增選單以管理材質集與烘焙機選擇

  在「材質集合清單」和「網格貼圖烘焙器」視窗中，新增了一個小動作選單，幫助複製和反轉選取。

* &amp;lbrack;烘焙模式&amp;rbrack;根據材質集分割烘焙器選擇列表

* &amp;lbrack;烘焙模式&amp;rbrack;依材質集拆分常用設定

* &amp;lbrack;烘焙模式&amp;rbrack;載入高多邊形與籠狀網格，且不凍結介面

* &amp;lbrack;烘焙模式&amp;rbrack;使用視窗進度條來顯示網格載入

* &amp;lbrack;烘焙模式&amp;rbrack; 在烘焙日誌中新增網格載入狀態

* &amp;lbrack;烘焙模式&amp;rbrack;允許在烘焙時在視窗中旋轉網格

* &amp;lbrack;烘焙模式&amp;rbrack;根據目前網格視窗可見度設定烘焙順序

* &amp;lbrack;烘焙模式&amp;rbrack;在視窗中顯示隱含烘焙籠

  當不使用自訂籠狀網格檔案時，會自動產生籠狀網格並在視窗中顯示。 它的大小會根據烘焙共用設定的最大正面距離參數來決定。 籠狀網格用來表示低多邊形與高多邊形匹配的距離。

* &amp;lbrack;烘焙模式&amp;rbrack;在烘焙日誌中顯示網格名稱匹配列表以按名稱匹配

* &amp;lbrack;烘焙模式&amp;rbrack;使用中性材質在視口中顯示 3D 模型

* &amp;lbrack;烘焙模式&amp;rbrack;在烘焙模式下停用引擎計算

* &amp;lbrack;烘焙模式&amp;rbrack;烘焙過程中退出應用程式時會顯示警告

* &amp;lbrack;Bakers&amp;rbrack;更新抗鋸齒設定標籤

  抗鋸齒設定值已改名為「超取樣」，並明確標示乘數以說明其行為。

* &amp;lbrack;Bakers&amp;rbrack;將 bakers 更新至 2.5.7 版本。

* &amp;lbrack;USD&amp;rbrack;匯入與匯出通用場景描述（USD）檔案

* &amp;lbrack;USD&amp;rbrack;在選擇美元檔案時，新增專案視窗中新增美元選項

* &amp;lbrack;USD&amp;rbrack; 新增範圍與變體選擇視窗

  匯入 USD 檔案時，點擊新專案或專案設定視窗中的變更按鈕，可以選擇要匯入 USD 檔案的哪部分及變體。

* &amp;lbrack;USD&amp;rbrack;新增分區層級選項

  當你建立包含細分的 USD 網格檔案的新專案時，可以用滑桿選擇細分的層級。 專案將使用細分網格來建立。 關卡可以透過專案設定來修改。

* &amp;lbrack;USD&amp;rbrack;匯入特定框架的美元蒙皮網格

  在建立包含動畫的 USD 網格檔案的新專案時，可以使用反映嵌入時間軸序列的滑桿選擇影格。 框架可以透過專案設定（Project Configuration）來修改。

* &amp;lbrack;USD&amp;rbrack;&amp;lbrack;Export&amp;rbrack; 新增匯出美元檔案的選項

  在「匯出材質」視窗新增「匯出美元」勾選框。 勾選後，允許匯出 USD 檔案以及使用任何範本的貼圖。

* &amp;lbrack;USD&amp;rbrack;&amp;lbrack;Export&amp;rbrack; 將 USD 檔案格式加入網格匯出

* &amp;lbrack;USD&amp;rbrack;將現有的「USD PBR Metal Roughness」出口預設更明確地命名

  先前稱為「USD PBR Metal Roughness」的美元匯出範本，仍可透過 Export textures > Output 模板> USDz（Apple AR）存取。

* &amp;lbrack;自動展開&amp;rbrack;為包裝添加鎖頭方向

  新增自動展開設定選項，允許在使用包裝功能時保留現有 UV 島的方向。 可透過新專案>自動展開選項>UV島嶼方向存取。

* &amp;lbrack;Physical Size&amp;rbrack;新增設定以自動在填充效果/圖層中使用 Physical Size

  新增了在使用具有嵌入物理尺寸的材料時自動切換到物理尺寸尺度的選項。 可透過新專案或透過編輯專案設定>>物理尺寸>切換填充層縮放至實體尺寸來啟用。

* &amp;lbrack;物理尺寸&amp;rbrack;曝光物理尺寸以進行紫外線投射

  現在 UV 投影支援實體尺寸縮放功能——它能根據網格的物理尺寸自動調整材質大小。 可透過填充圖層的縮放>物理尺寸或效果屬性視窗中選擇。

* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 允許查詢應用程式版本

* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;JavaScript&amp;rbrack; Update API 以匹配新的烘焙參數

* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; Baking module： edit baking parameters

* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; Baking module： launch/cancel baking

* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; Baking module： select curvature method

* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; Baking module： selection of bakers/uv tiles

* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 烘焙模組：同步所有材質集的烘焙設定

* &amp;lbrack;SVT&amp;rbrack;啟用 AMD GPU 上的稀疏硬體支援

  現在 AMD GPU 可以啟用稀疏虛擬材質系統的硬體加速。 此設定會在一般偏好設定中自動啟用。

* &amp;lbrack;投影&amp;rbrack; 重新命名 圓柱投影參數

  參數「圓柱蓋剔除」已改名為「背面剔除」，以更好地表示其動作。 相關的提示也已相應調整。

* &amp;lbrack;Project&amp;rbrack; 將應用程式版本存於專案中，並透過腳本擷取

  自 8.2 版本起，應用程式的版本現在儲存在 spp 檔案中。 此版本號可透過 Python API 專案模組中的函式 last_saved_substance_painter_version（） 取得。 對於 8.2 之前製作的專案，回傳的值將為空值。

* &amp;lbrack;Import&amp;rbrack;改善3D模型的一般匯入時間

  我們改善了網格的一般匯入時間。 例如，在烘焙時，能縮短載入高多邊形網格時的等待時間。 此優化特別適用於 OBJ 檔案的載入。

**修正：**

* &amp;lbrack;Crash&amp;rbrack;在特定堆疊中切換濾波器頻道

* &amp;lbrack;Mac&amp;rbrack;&amp;lbrack;M1&amp;rbrack; 在建立填充層並離開層堆疊時會崩潰

  這個問題可以透過更新到 Mac OS 13（Ventura）來解決。

* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack;使用 ui.add_dock_widget（） 錯誤型別時會當機

* &amp;lbrack;Baking&amp;rbrack;烘焙失敗時日誌中出現不完整錯誤訊息

* &amp;lbrack;烘焙&amp;rbrack;烘焙完成時記憶體不會被釋放

* &amp;lbrack;Engine&amp;rbrack;紋理快取在改變效果可見性時不會更新

* &amp;lbrack;Export&amp;rbrack; 2D View 隨機匯出均勻地圖

* &amp;lbrack;Project&amp;rbrack;儲存大型網格專案時記憶體配置錯誤

* &amp;lbrack;Viewport&amp;rbrack;TAA 在某些情況下會在繪畫時產生雜訊

**已知問題：**

* &amp;lbrack;色彩管理&amp;rbrack;在 Linux 上使用 ACE 進行 HDR 色彩空間轉換會產生壓縮色彩
* &amp;lbrack;層疊疊&amp;rbrack;輸入來源不會在每層儲存

### 8.2.0

*（發布日期：2022* 年 10 月 6 日）摘要： **重大釋出，新增了新入門面板（新增歡迎面板與新功能面板）、匯出至 SBSAR、資料夾效果、多項生活品質改進及錯誤修正。**

**補充：**

* &amp;lbrack;入門&amp;rbrack;歡迎新用戶的入門小組

  新增一個歡迎畫面，當新自訂用戶第一次打開 Painter 時。

* &amp;lbrack;Onboarding&amp;rbrack;新增面板提升新功能可發現性

  新增了一個「新增內容」畫面，顯示主要新功能。 在重大更新後首次開啟 Painter 時會自動顯示，並可透過「說明>新內容」再次存取。

* &amp;lbrack;Onboarding&amp;rbrack; 重新命名舊版 歡迎來到「主畫面」

  舊的歡迎畫面改名為主畫面，以避免與新的歡迎畫面混淆。

* &amp;lbrack;UI&amp;rbrack;解決高DPI螢幕的縮放問題

  提升 Painter 介面在高畫質螢幕上的適應性，並可自訂顯示縮放。

* &amp;lbrack;UI&amp;rbrack; 避免使用者介面中持續出現錯誤訊息

  過去專案的錯誤訊息現在已從底部狀態列移除。

* &amp;lbrack;UI&amp;rbrack;重製儲存選單

  額外的存檔選項現在會被分組在子選單中，有些則為了保持一致性而重新命名。

* &amp;lbrack;UI&amp;rbrack;儲存並匯出/分享 UI 版面

  在視窗選單中新增了將 UI 佈局儲存成檔案並重新載入的新動作。 繪畫和渲染版面會分別儲存。 「substance_painter.ui」也新增了各種功能，可以儲存、重置及載入 UI 版面。

* 新增複製貼上動作來混合模式或圖層的透明度

  在圖層右鍵選單新增了「混合選項」。 它允許將所有通道的混合模式與透明度從一圖層複製貼上到另一層。

* 對圖層的所有通道套用混合模式/不透明度

  新增了右鍵功能，讓圖層的混合模式和透明度能把目前點擊的設定套用到所有通道。

* 用鍵盤快捷鍵重新載入網格（CTRL+SHIFT+R）

  新增了一個可編輯的捷徑，可以重新載入網格檔案，並保留最後可用的設定。 也可以透過編輯>重新匯入網格來存取。

* 將物質參數重置為預設

  在 .sbsar 資源底部的屬性中新增了一個按鈕，可以將資源重置為預設值。

* 將畫筆重置為預設

  在屬性的筆刷區塊新增了一個選單，可以重置成預設的基本筆刷。

* 右鍵點擊可將個別物質參數重置為預設值

  新增了透過右鍵點擊重設 .sbsar 資源中個別參數的功能。

* &amp;lbrack;資產面板&amp;rbrack;「釘選」最愛資產，顯示在資產面板頂端

  新增了一個右鍵功能，可以將素材置選為收藏，置於面板頂端。 你也可以透過「已儲存搜尋」查看所有喜愛的素材。

* &amp;lbrack;資產面板&amp;rbrack;刪除、重新載入及重新命名資產

  新增了右鍵選單選項，可以刪除、重新載入及重新命名使用者資料庫中的資產。 它們會直接從磁碟上的資料庫位置刪除，並從原始位置重新載入。 像 .abr 或 .sbsar 這類套件中的資產無法單獨編輯。

* &amp;lbrack;色彩選擇&amp;rbrack;將混合模式加入色彩選擇效果

* &amp;lbrack;Layer Stack&amp;rbrack;在濾鏡上加入混合模式和不透明度

* &amp;lbrack;Layer stack&amp;rbrack;允許填充層/效果的平鋪值大於 128

* &amp;lbrack;層堆疊&amp;rbrack;用於填充層/效果中圓柱形投影的圓柱蓋

  填充層屬性中的圓柱投影現在可以移除圓柱蓋。

* &amp;lbrack;Log&amp;rbrack;如果網格部分位於負空間，嘗試建立 UV Tile 專案時會顯示錯誤訊息

  新增了更清楚的錯誤訊息，因為 UV 部分位於負空間，導致無法建立 UV Tile 專案。

* &amp;lbrack;Project&amp;rbrack;開啟專案時，請以錯誤訊息「data too renew」標示版本

  當開啟對該應用程式來說過於新的專案時，錯誤訊息會顯示專案版本，方便辨識正確的應用程式版本。

* &amp;lbrack;Viewport&amp;rbrack; 允許從下方照亮網格

  在顯示設定>相機>環境設定中新增了一個環境對齊參數，讓環境貼圖的光照在設定為「本地」時與相機對齊。

* &amp;lbrack;視窗&amp;rbrack;在視窗中查看 R、G、B 和 Alpha（單人顯示模式）

  在「顯示設定」>「視窗設定」>「通道顯示」中，有一個新的色彩通道設定，允許在單一顯示模式下只顯示通道的 R、G、B 或 Alpha 成分。

* &amp;lbrack;Shader&amp;rbrack;允許在材質分層著色器中將使用者通道設定為 RGBA

  在著色器中設定材質分層的 Texture Set 通道設定時，現在可以指定通道格式以偏離預設值。 這讓它能特別地請求彩色使用者通道，而非僅灰階。

* &amp;lbrack;Export&amp;rbrack; 允許將貼圖匯出為 SBSAR

  透過檔案 > 匯出材質視窗匯出貼圖時，可以選擇 SBSAR（Substance Archive）檔案格式來重新組合這些材質。 SBSAR 的內容由所使用的輸出範本驅動。 SBSAR 檔案格式也可以在匯出預設中設定。 使用混合配置（SBSAR + 其他格式）時，針對 SBSAR 的貼圖會被分組，其餘則與之一併匯出。

* &amp;lbrack;Export&amp;rbrack; EXR 檔案格式的 16 位元選項

  匯出 EXR 材質檔時，現在可以在匯出材質視窗中選擇 16f 位元（半浮點）或 32 位元（浮點）（匯出設定和匯出預設皆可）。 舊專案和舊匯出預設會預設為 16f 位元，以反映舊有的行為。

* &amp;lbrack;Python&amp;rbrack; 新增事件以知道紋理集何時被修改

  新的「substance_painter.event.TextureStateEvent」可以讓你知道材質集是否因繪圖筆觸、新增通道或移除通道而被修改。

* &amp;lbrack;Python&amp;rbrack; 允許在貼圖集設定中取得並設定網格貼圖資源

  「substance_painter.project」模組新增了用來取得和設定網格貼圖資源的功能。 這些函式可以用來更新貼圖集設定所參考的網格貼圖。

* &amp;lbrack;Plugins&amp;rbrack; 移除取得其他 JS 插件的選項

  移除了取得 JavaScript 外掛的選項，因為它們是托管在已棄用的 Share 網站上。

* &amp;lbrack;內容&amp;rbrack; 新增 Roblox 範本並匯出預設

  新增了 Roblox 的「材質變體」和「表面外觀」專案範本及匯出預設，讓 PBR 材質匯出到 Roblox 變得更簡單。 範本可透過檔案>新專案視窗存取。

* 更新 Substance Engine 至最新版本（8.6.3）

* &amp;lbrack;Steam&amp;rbrack;為 Apple Silicon 晶片組（Apple M1 / M2）優化版本

**修正：**

* 使用 16k EXR 時會當機

* &amp;lbrack;Crash&amp;rbrack; Ctrl Z 刪除著色器實例後

* &amp;lbrack;Iray&amp;rbrack;IoR 對某些著色器被封鎖為 1

* &amp;lbrack;Win&amp;rbrack\lbrack;Baking&amp;rbrack; 某些高多邊形無法載入

* &amp;lbrack;色彩管理&amp;rbrack;在含濾鏡的介面中色彩空間名稱錯誤

* &amp;lbrack;Python&amp;rbrack;由匯入函式回傳的資源物件沒有型別

  在 Python 匯入 Substance 套件時，函式會回傳套件本身，而非其圖形。 資源模組現在提供函式與參數，以擷取 Substance 套件的圖。

**已知問題：**

* &amp;lbrack;色彩管理&amp;rbrack;在 Linux 上使用 ACE 進行 HDR 色彩空間轉換會產生壓縮色彩
* &amp;lbrack;層疊疊&amp;rbrack;輸入來源不會在每層儲存
* &amp;lbrack;繪畫&amp;rbrack;時間抗鋸齒在某些情況下會在繪畫時產生偽影
* &amp;lbrack;Export&amp;rbrack; 2D View 隨機匯出均勻地圖

### 8.1.3

*（發布日期：2022* 年 8 月 25 日）摘要： **小規模錯誤修正釋出**

**補充：**

* Iray SDK 1.6 更新

**修正：**

* &amp;lbrack;著色器&amp;rbrack;舊有著色器故障時崩潰
* &amp;lbrack;材料分層&amp;rbrack;重新開啟專案時，材料可能會消失

**已知問題：**

* &amp;lbrack;色彩管理&amp;rbrack;在 Linux 上使用 ACE 進行 HDR 色彩空間轉換會產生壓縮色彩
* &amp;lbrack;層疊疊&amp;rbrack;輸入來源不會在每層儲存
* &amp;lbrack;Crash&amp;rbrack; Ctrl Z 刪除著色器實例後
* &amp;lbrack;Iray&amp;rbrack;IoR 對某些著色器被封鎖為 1

### 8.1.2

*（發布日期：2022* 年 7 月 19 日）摘要： **小規模錯誤修正釋出**

**補充：**

* &amp;lbrack;自動展開&amp;rbrack;新增選項「優化有機網格」以選擇分割演算法
* &amp;lbrack;物理尺寸&amp;rbrack;在新專案與專案配置中顯示單元選項
* &amp;lbrack;色彩管理&amp;rbrack;使用 ACE 時預設使用顯示器顯示
* &amp;lbrack;Color Management&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 在建立專案時請考慮 ACE env-var 預設檔案
* &amp;lbrack;色彩管理&amp;rbrack;設定變更時，在新專案視窗中重置色彩管理設定
* &amp;lbrack;色彩管理&amp;rbrack;當 env-var 存在時，請停用 OCIO 設定存取
* &amp;lbrack;色彩管理&amp;rbrack;當參數不再存在時，安全更新 ACE 設定
* 更新 Substance Engine 至 8.6.0 版本
* &amp;lbrack;Export&amp;rbrack; 新增 GLTF 匯出預設並支援 Displacement
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 取得資源資訊（含自訂元資料）
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 新增函式到 Texture Set 的網格名稱查詢清單
* &amp;lbrack;內容&amp;rbrack; 新增 Blender 模板並匯出預設

**修正：**

* &amp;lbrack;MacOS&amp;rbrack;在某些情況下啟動 Iray 時會當機
* &amp;lbrack;縮圖&amp;rbrack;架子縮圖無法正確載入
* 多個紫外線通道會被忽略
* &amp;lbrack;自動展開&amp;rbrack;分割長島時不必要的計算
* &amp;lbrack;自動展開&amp;rbrack;選項避免未考慮的拉長島嶼
* &amp;lbrack;自動展開&amp;rbrack;重新包裝 UV 時會損失額外資料（頂點顏色）
* &amp;lbrack;UI&amp;rbrack;在啟用色彩管理時，屬性視窗中的水平捲動列
* &amp;lbrack;色彩管理&amp;rbrack;OCIO 設定缺少substance_3d_painter_standard_srgb角色
* &amp;lbrack;Generator&amp;rbrack; 使用者資料的錯誤使用「被禁用」
* &amp;lbrack;色彩管理&amp;rbrack;色彩空間「不相容」下拉選單不應該是可點擊的
* &amp;lbrack;色彩管理&amp;rbrack;&amp;lbrack;Shader&amp;rbrack; sRGB 覆寫定義不再有效
* &amp;lbrack;Generator&amp;rbrack;使用者資料的錯誤使用「禁用」
* &amp;lbrack;Layer stack&amp;rbrack;用 UV Tiles 專案來預覽
* &amp;lbrack;Shader&amp;rbrack;API 文件尚未完全更新 Bent Normals
* &amp;lbrack;Export&amp;rbrack;&amp;lbrack;互通性&amp;rbrack; 無法傳送特殊字元給 Stager
* &amp;lbrack;內容&amp;rbrack;有些筆刷預設的縮圖是空白或太暗

**已知問題：**

* &amp;lbrack;色彩管理&amp;rbrack;在 Linux 上使用 ACE 進行 HDR 色彩空間轉換會產生壓縮色彩
* &amp;lbrack;層疊&amp;rbrack;輸入來源不會儲存在每層
* &amp;lbrack;Crash&amp;rbrack; Ctrl Z 刪除著色器實例後
* &amp;lbrack;Iray&amp;rbrack;IoR 對某些著色器被封鎖為 1
* &amp;lbrack;著色器&amp;rbrack;舊有著色器故障時崩潰

### 8.1.1

*（發布日期：2022* 年 6 月 28 日）摘要： **小規模版本熱修**

**補充：**

* &amp;lbrack;Layer Stack&amp;rbrack;Alt 點擊遮罩後不會再取消選擇效果了

**修正：**

* &amp;lbrack;Crash&amp;rbrack; 以個人檢視模式開啟舊專案
* &amp;lbrack;Crash&amp;rbrack; 在屬性中刪除產生器
* &amp;lbrack;貼圖集設定&amp;rbrack;法線/環境遮蔽混合及高度法線法線方法都被破壞了
* &amp;lbrack;Export&amp;rbrack;使用擴散填充導出貼圖會渲染黑色貼圖

**已知問題：**

* &amp;lbrack;MacOS&amp;rbrack;在蒙特雷啟動 Iray 時當機
* &amp;lbrack;預覽縮圖&amp;rbrack;使用錨點時，簡化縮圖不會更新
* &amp;lbrack;色彩管理&amp;rbrack;在 Linux 上使用 ACE 進行 HDR 色彩空間轉換會產生壓縮色彩

### 8.1.0

*（發布日期：2022*&#x200B;年6月7日）摘要： **重大版本，支援ICC，基於實體尺寸資料進行材料縮放，新增烘焙師，彩色滴管改良，以及一系列額外內容**

**補充：**

* &amp;lbrack;色彩管理&amp;rbrack;新增 Adobe Color Engine （ACE） 對 ICC 設定檔的支援
* &amp;lbrack;色彩管理&amp;rbrack;新增對「Adobe 98 RGB」作為 ICC 工作色彩空間的支援
* &amp;lbrack;色彩管理&amp;rbrack;允許透過設定檔設定 ACE/ICC 設定
* &amp;lbrack;色彩管理&amp;rbrack;允許在 Color Picker 與 Legacy 模式中輸入線性色彩值
* &amp;lbrack;色彩管理&amp;rbrack;允許指定用於在使用者介面外選取顏色的色彩設定檔
* &amp;lbrack;色彩管理&amp;rbrack;記住視窗中最後選擇的顯示值
* &amp;lbrack;色彩管理&amp;rbrack;&amp;lbrack;Substance&amp;rbrack; 讓產生器/濾鏡在色彩管理中正常運作
* &amp;lbrack;色彩管理&amp;rbrack;&amp;lbrack;Substance&amp;rbrack; 新增色彩空間覆蓋關鍵字 $working 和 $standardsrgb
* &amp;lbrack;物理尺寸&amp;rbrack;&amp;lbrack;Engine&amp;rbrack; 從網格中擷取物理大小資訊
* &amp;lbrack;物理尺寸&amp;rbrack;&amp;lbrack;Engine&amp;rbrack; 物理大小計算
* &amp;lbrack;Physical Size&amp;rbrack; 在使用者介面中暴露使用實體尺寸的選項
* &amp;lbrack;Physical Size&amp;rbrack; 在視窗中新增視覺輔助
* &amp;lbrack;烘焙&amp;rbrack;加高烘焙師
* &amp;lbrack;烘焙&amp;rbrack;加入彎曲法線麵包師
* &amp;lbrack;Baking&amp;rbrack; 加入不透明度烘焙機
* &amp;lbrack;滴管&amp;rbrack;滑鼠旁邊的新彩色滴管預覽，色彩管理
* &amp;lbrack;滴管&amp;rbrack;重新打開時，顏色選擇面板會回到最後的位置
* &amp;lbrack;滴管&amp;rbrack;物料拾取機的新圖示
* &amp;lbrack;滴管&amp;rbrack;色彩管理，控制色彩選擇器的頻道預覽
* &amp;lbrack;滴管&amp;rbrack;為吸管新增點擊選擇功能
* &amp;lbrack;眼滴管&amp;rbrack;物料選擇器不再啟動非啟動通道
* &amp;lbrack;滴管&amp;rbrack;允許使用吸管並取得快捷鍵
* &amp;lbrack;Eye dropper &amp;rbrack;吸管會接收相關頻道（如適用）
* &amp;lbrack;滴管&amp;rbrack;進入色彩選擇模式會停用所有捷徑
* &amp;lbrack;滴管&amp;rbrack;移除六角格欄位的自動選擇功能
* &amp;lbrack;滴管&amp;rbrack;使用物料選擇器時不要關閉面板
* &amp;lbrack;滴管&amp;rbrack;當頻道無法選取時，新的停用狀態
* &amp;lbrack;Export&amp;rbrack; 將 tangent 屬性加入 glTF export
* 更新 Substance Engine 至 v8.4
* 自動展開更新至 0.9.0
* 更新至Qt 5.15.8
* 更新至 Python 3.9
* &amp;lbrack;Shader&amp;rbrack; 新增對彎曲法線著色的支援
* &amp;lbrack;MacOS&amp;rbrack;支援 3DConnexion SpaceMouse
* &amp;lbrack;Python&amp;rbrack;請說明API中使用的Python版本
* &amp;lbrack;內容&amp;rbrack;新增6種3D音效及105個預設音色
* &amp;lbrack;內容&amp;rbrack;20張新的垃圾搖滾地圖和2種布料摺疊圖案
* &amp;lbrack;Content&amp;rbrack; 更新「Mesh maps」匯出預設以使用新的烘焙工具
* &amp;lbrack;內容&amp;rbrack;模糊斜率與變形濾鏡取決於材質集的解析度
* &amp;lbrack;Content&amp;rbrack;更新範例專案以使用三位新烘焙師

**修正：**

* &amp;lbrack;glTF&amp;rbrack;無法以特殊字元開啟 glTF
* &amp;lbrack;引擎與rbrack;具有各向異性與SVT失效的雜訊
* &amp;lbrack;MacOS&amp;rbrack;&amp;lbrack;M1&amp;rbrack; 智慧材質無法正確顯示
* &amp;lbrack;網格處理&amp;rbrack;無法從 Modeler 匯入網格
* &amp;lbrack;UI&amp;rbrack;新專案視窗中啟用色彩管理的水平滾動條
* &amp;lbrack;色彩管理&amp;rbrack;部分 OCIO 設定中缺少工作空間值
* &amp;lbrack;色彩管理&amp;rbrack;視窗中的筆刷預覽並非色彩管理
* &amp;lbrack;SpaceMouse&amp;rbrack;Pivot 不會因焦點變更而立即更新，有時甚至會從模型中移除
* &amp;lbrack;Export&amp;rbrack;&amp;lbrack;USD&amp;rbrack;匯出的美元檔案結構錯誤
* &amp;lbrack;USD&amp;rbrack;出口時的環境遮蔽問題
* &amp;lbrack;內容&amp;rbrack;更新縮圖網格以符合預覽球體範例專案

**已知問題：**

* 使用擴散填充匯出材質會渲染黑色貼圖
* 正常/環境遮蔽混合壞掉了
* &amp;lbrack;MacOS&amp;rbrack;在某些罕見情況下啟動 Iray 時會當機
* &amp;lbrack;預覽縮圖&amp;rbrack;簡化縮圖在使用錨點時不會更新
* &amp;lbrack;色彩管理&amp;rbrack;在 Linux 上使用 ACE 進行 HDR 色彩空間轉換會產生壓縮色彩

## 版本7

### 7.4.3

*（發布日期：2022* 年 4 月 11 日）摘要： **支援 3Dconnexion SpaceMouse 於 2D 視窗中的錯誤修正**

**補充：**

* &amp;lbrack;SpaceMouse&amp;rbrack;支援 3DConnexion SpaceMouse 於 2D 視窗中

**修正：**

* &amp;lbrack;色彩選擇器&amp;rbrack;無法在十六進位欄位中書寫
* &amp;lbrack;色彩管理&amp;rbrack;投影模式下使用的資源不會在覆蓋層中被調色
* &amp;lbrack;色彩管理&amp;rbrack;錯誤不會以日誌報告
* &amp;lbrack;SpaceMouse&amp;rbrack; 若使用者沒有 SpaceMouse，請移除通用錯誤訊息
* &amp;lbrack;SpaceMouse&amp;rbrack;載入專案時，樞軸點總是隱藏的
* &amp;lbrack;Bakers&amp;rbrack;「平均法線」設定在 UV 圖塊專案中沒有影響
* &amp;lbrack;UV Tile&amp;rbrack;當用不同圖塊重新載入網格時，非啟用的 UV 圖塊覆蓋層會消失
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 遠端腳本壞了
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 多個通道無法從 API 查詢，且會產生錯誤
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 使用 ProjectEditionEntered 事件時當機
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 呼叫 get_active_stack（） 時崩潰

**已知問題：**

* 3Dconnexion SpaceMouse 不支援 MacOS
* &amp;lbrack;UI&amp;rbrack;水平滾動列，部分情況下在新專案視窗中顯示顏色管理功能
* &amp;lbrack;Mac M1&amp;rbrack;智慧材質未正確顯示

### 7.4.2

*（發布日期：2022* 年 3 月 8 日）摘要： **錯誤修正，支援 3Dconnexion SpaceMouse 及色彩管理（OCIO）改進**

**補充：**

* &amp;lbrack;SpaceMouse&amp;rbrack;&amp;lbrack;Windows&amp;rbrack;在 3D Viewport 中支援 3Dconnexion SpaceMouse 以進行導航
* &amp;lbrack;SpaceMouse&amp;rbrack;&amp;lbrack;Windows&amp;rbrack;3D Viewport 中 Pro 與企業版 SpaceMouse 模型的基本快捷鍵/快捷鍵
* &amp;lbrack;SpaceMouse&amp;rbrack;&amp;lbrack;Windows&amp;rbrack;3D 視窗中的專用旋轉中心圖示
* &amp;lbrack;色彩管理&amp;rbrack;使用 OCIO 設定中的角色來更改預設設定
* &amp;lbrack;色彩管理&amp;rbrack;色彩管理屬性視窗中的色彩管理
* &amp;lbrack;色彩管理&amp;rbrack;材質預覽時的屬性視窗進行色彩管理
* &amp;lbrack;色彩管理&amp;rbrack;在色彩選擇器中管理色片
* &amp;lbrack;色彩管理&amp;rbrack; 新增設定以定義標準 sRGB 色彩空間
* &amp;lbrack;色彩管理&amp;rbrack;從 OCIO 設定中加入標準的 sRGB 色彩空間，在色彩選擇器中加入顯示選擇器列表
* &amp;lbrack;色彩管理&amp;rbrack;色彩空間覆蓋選單的改進
* &amp;lbrack;色彩管理&amp;rbrack; 允許在顯示設定中覆寫環境地圖色彩空間
* &amp;lbrack;色彩管理&amp;rbrack;根據目前顯示繪製色彩選擇器漸層
* &amp;lbrack;色彩管理&amp;rbrack;在色彩編輯器中預設夾取 HDR 值
* &amp;lbrack;色彩管理&amp;rbrack;在 Legacy 模式下使用直通（無色彩空間）來控制濾鏡
* &amp;lbrack;色彩管理&amp;rbrack;在色彩編輯器中限制漸層顯示以匹配 &amp;lbrack;0-1&amp;rbrack; 範圍
* &amp;lbrack;色彩管理&amp;rbrack;在舊有模式的色彩選擇器中隱藏顯示選擇器
* &amp;lbrack;色彩管理&amp;rbrack;讓色彩選擇器的十六進位欄位始終在 sRGB 色彩空間中
* &amp;lbrack;色彩管理&amp;rbrack; 停用資料通道的色彩選擇器顯示下拉選單
* &amp;lbrack;Optimization&amp;rbrack;Warp 網格僅重新計算覆蓋的 UV 磚塊
* &amp;lbrack;Export&amp;rbrack;允許匯出 Sketchfab、USD 及 glTF 的 UV 圖磚專案
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 允許更改音色映射函數

**修正：**

* &amp;lbrack;Sketchfab&amp;rbrack;更新現有模型會產生新模型
* &amp;lbrack;Sketchfab&amp;rbrack;搜尋先前更新模型時當機
* 匯出成美元時當機
* 在 Geometry Mask 建立新著色器實例或幾何體被隱藏時會當機
* &amp;lbrack;匯入資產視窗&amp;rbrack;變更匯入資源類型時會崩潰
* 法線網格貼圖在層堆疊中使用時會被反轉
* &amp;lbrack;Substance&amp;rbrack;使用者資料混合模式不被考慮
* &amp;lbrack;色彩管理&amp;rbrack;檔名中帶有色彩空間的位圖會匯入為 UV 圖塊序列
* &amp;lbrack;色彩管理&amp;rbrack;Substance圖的色彩管理輸出出現在錯誤的色彩空間
* &amp;lbrack;色彩管理&amp;rbrack;多邊形填充工具顯示錯誤的顏色
* &amp;lbrack;色彩管理&amp;rbrack;ACES tonemapper 會套用到單聲道模式的通道
* &amp;lbrack;色彩管理&amp;rbrack;工具預覽球體光照並非色彩管理
* &amp;lbrack;色彩管理&amp;rbrack;&amp;lbrack;Export&amp;rbrack; 轉換地圖套用錯誤轉換
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack;&amp;lbrack;Color Management&amp;rbrack; 使用 template 與 OCIO 環境變數建立的專案皆處於 Legacy 模式
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 啟動時無法使用 JavaScript 的 evaluate 函式
* &amp;lbrack;3D Adobe Offer&amp;rbrack;使用預設不支援語言的區域設定時無法啟動 Painter

**已知問題：**

* 3Dconnexion SpaceMouse 不支援 MacOS
* &amp;lbrack;UI&amp;rbrack;水平滾動列，部分情況下在新專案視窗中顯示顏色管理功能
* &amp;lbrack;Bakers&amp;rbrack;「平均法線」設定在 UV 圖塊專案中沒有影響
* &amp;lbrack;Mac M1&amp;rbrack;智慧材質無法正確顯示
* &amp;lbrack;色彩管理&amp;rbrack;投影模式下使用的資源不會在覆蓋層中被調色
* &amp;lbrack;色彩選擇器&amp;rbrack;無法在十六進位欄位中書寫

### 7.4.1

*（發布日期：2021* 年 12 月 14 日）摘要： **修正錯誤並加強色彩管理**

**補充：**

* &amp;lbrack;色彩管理&amp;rbrack;在匯出檔名中使用資料角色
* &amp;lbrack;色彩管理&amp;rbrack;預設在新專案與專案設定視窗中選取 OCIO 時，展開色彩管理區塊
* &amp;lbrack;色彩管理&amp;rbrack; 在舊有模式下新增 ACES tonemapper
* &amp;lbrack;色彩管理&amp;rbrack;調整預設設定
* &amp;lbrack;色彩管理&amp;rbrack;&amp;lbrack;Export&amp;rbrack; 在資料通道的檔名中填$colorSpace
* &amp;lbrack;Export&amp;rbrack; 將 UV 圖塊專案匯出到 Stager
* &amp;lbrack;互通性&amp;rbrack;不支援 Steam 和 Substance 版本
* &amp;lbrack;互通性&amp;rbrack;允許將 UV 圖塊專案傳送至 Stager

**修正：**

* &amp;lbrack;MacOS&amp;rbrack;&amp;lbrack;Crash&amp;rbrack; Painter 不會以 Catalina 開頭
* &amp;lbrack;色彩管理&amp;rbrack;&amp;lbrack;Crash&amp;rbrack; 在用戶頻道上使用資料型別/色彩管理時隨機當機
* &amp;lbrack;色彩管理&amp;rbrack;作為遮罩灰階使用的資源顯示色彩空間 新選單
* &amp;lbrack;色彩管理&amp;rbrack;使用者通道在傳統模式 + 單視圖中，視窗中較暗
* &amp;lbrack;色彩管理&amp;rbrack;環境貼圖在 iRay 中使用時始終是線性的
* &amp;lbrack;色彩管理&amp;rbrack;色彩選擇器在舊有模式下無法為資料通道選擇正確值
* &amp;lbrack;色彩管理&amp;rbrack;在 Substance 的舊有模式下，顏色選擇器壞掉了
* &amp;lbrack;色彩管理&amp;rbrack;在視窗切換單通道視圖時，使用下拉選單時會顯示出正確的色彩空間
* &amp;lbrack;色彩管理&amp;rbrack;在舊有模式下，匯出對色彩管理的用戶頻道套用錯誤的轉換
* 切換回材質視圖時，單視遮罩下的筆觸不會顯示
* &amp;lbrack;Export&amp;rbrack;轉換後的地圖不會匯出為色彩管理頻道
* &amp;lbrack;紋理集&amp;rbrack;在更名使用者通道中缺少原始名稱的工具提示
* &amp;lbrack;Steam&amp;rbrack;在檢查 Steam 檔案完整性時缺少檔案

**已知問題：**

* &amp;lbrack;Mac M1&amp;rbrack;智慧材質無法正確顯示

### 7.4.0

*（發行日期：2021*&#x200B;年11月24日）摘要： **重大發行。 引入第一版色彩管理、2D 或 3D 脫離底座、自動 UV 展開以避免拉長島嶼的新選項、從 Python API 呼叫 JavaScript 函式及新增內容**

**補充：**

* &amp;lbrack;色彩管理&amp;rbrack;支援色彩管理 OpenColorIO 版本 2
* &amp;lbrack;色彩管理&amp;rbrack; 將色彩管理設定加入專案設定
* &amp;lbrack;色彩管理&amp;rbrack;開啟專案時關於色彩管理設定變更的警告視窗
* &amp;lbrack;色彩管理&amp;rbrack;若選取無效的 OCIO 設定檔，則顯示錯誤訊息
* &amp;lbrack;色彩管理&amp;rbrack;允許以 OCIO 環境變數覆蓋設定
* &amp;lbrack;色彩管理&amp;rbrack;預設整合多種 OCIO 配置與應用程式
* &amp;lbrack;色彩管理&amp;rbrack;從匯入的點陣圖檔名中提取色彩空間名稱
* &amp;lbrack;色彩管理&amp;rbrack;允許在屬性視窗中用一個色彩空間覆蓋設定中的色彩空間
* &amp;lbrack;色彩管理&amp;rbrack; 在材質集設定中新增色彩管理選項
* &amp;lbrack;色彩管理&amp;rbrack;&amp;lbrack;視窗&amp;rbrack; 允許分別管理2D與3D視圖的色彩管理
* &amp;lbrack;色彩管理&amp;rbrack;載入並轉換環境貼圖為工作色彩空間
* &amp;lbrack;色彩管理&amp;rbrack;根據當前色彩空間調整色彩選擇器與編輯器
* &amp;lbrack;色彩管理&amp;rbrack;允許在視窗中選擇顯示轉換色彩空間，並開啟新的下拉選單
* &amp;lbrack;色彩管理&amp;rbrack;在 Iray 渲染結果中套用顯示轉換
* &amp;lbrack;色彩管理&amp;rbrack;匯出具有不同色彩空間的貼圖
* &amp;lbrack;色彩管理&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 將環境變數（OCIO）中的色彩管理設定套用到新專案
* &amp;lbrack;Viewport&amp;rbrack; 允許將 2D 或 3D 視窗脫離對接
* &amp;lbrack;自動展開&amp;rbrack;避免長島的新選項
* &amp;lbrack;腳本 Python&amp;rbrack;從 Python API 呼叫 JavaScript 函式
* &amp;lbrack;新專案視窗&amp;rbrack;讓匯入的地圖區塊可摺疊
* &amp;lbrack;投影&amp;rbrack;&amp;lbrack;Warp&amp;rbrack; 允許在Warp設定中隱藏法線
* &amp;lbrack;內容&amp;rbrack;11張全新垃圾搖滾地圖
* &amp;lbrack;內容&amp;rbrack;8個新工具預設（拉鍊、緊繩、亮粉）
* &amp;lbrack;內容&amp;rbrack;8種新材料（疤痕、口袋等）
* &amp;lbrack;內容&amp;rbrack;1個新發電機（膨脹縮曲速）

**已知問題：**

* &amp;lbrack;Mac M1&amp;rbrack;智慧材質無法正確顯示
* &amp;lbrack;色彩管理&amp;rbrack;&amp;lbrack;Crash&amp;rbrack; 在用戶頻道上使用資料型別/色彩管理時隨機當機
* &amp;lbrack;色彩管理&amp;rbrack;色彩選擇器在舊有模式下無法為資料通道選擇正確值
* &amp;lbrack;色彩管理&amp;rbrack;&amp;lbrack;Iray&amp;rbrack; 在視窗啟用色彩管理時，將渲染儲存在EXR或TIFF中，且在視窗中啟用色彩管理，則永遠會以線性方式儲存
* &amp;lbrack;色彩管理&amp;rbrack;在遮罩中用作灰階的資源顯示錯誤的色彩空間選單
* &amp;lbrack;色彩管理&amp;rbrack;&amp;lbrack;Iray&amp;rbrack; 環境映射在 Iray 中使用時總是線性
* &amp;lbrack;色彩管理&amp;rbrack;&amp;lbrack;Export&amp;rbrack; 轉換後的地圖不會匯出為色彩管理通道
* &amp;lbrack;色彩管理&amp;rbrack;&amp;lbrack;Export&amp;rbrack;匯出忽略使用者通道是否在舊有模式下進行色彩管理

### 7.3.1

*（發布日期：2021*&#x200B;年11月24日）摘要： **錯誤修正**

**補充：**

* &amp;lbrack;投影&amp;rbrack;縮放應該只在物件空間中運作

**修正：**

* &amp;lbrack;Mac M1&amp;rbrack;材質層疊不工作
* &amp;lbrack;Mac M1&amp;rbrack;&amp;lbrack;投影&amp;rbrack;Warp 無法運作
* 微觀細節無法正確顯示
* &amp;lbrack;投影&amp;rbrack;&amp;lbrack;Crash&amp;rbrack; 切換到曲速模式，並用先前版本建立的圖層
* &amp;lbrack;投影&amp;rbrack;&amp;lbrack;Warp&amp;rbrack; 當轉換設定為世界空間時，翻轉功能無法運作
* &amp;lbrack;投影&amp;rbrack;&amp;lbrack;Warp&amp;rbrack;分割完成後仍保留分割選項
* &amp;lbrack;投影&amp;rbrack;&amp;lbrack;UV&amp;rbrack; 翻轉投影時樞軸點會被重置
* &amp;lbrack;Filter&amp;rbrack;烘焙燈光環境在重新載入或參數變更時會改變
* &amp;lbrack;互通性&amp;rbrack;不支援 Steam 和 Substance 版本
* &amp;lbrack;互通性&amp;rbrack;「在市場中瀏覽 3D 資產」按鈕應該總是在股票與市場 3D 標籤中開啟 CCD。

**已知問題：**

* &amp;lbrack;Mac M1&amp;rbrack;智慧材質無法正確顯示

### 7.3.0

*（發行日期：2021*&#x200B;年10月13日）摘要： **重大發行。 它包含了新的 3D 扭曲投影、新的圓柱投影、色彩選擇器的改進、Python API 的新函式以及錯誤修正**

**補充：**

* &amp;lbrack;投影&amp;rbrack;&amp;lbrack;Warp&amp;rbrack; 將3D warp曝光為一種新的投影模式
* &amp;lbrack;投影&amp;rbrack;&amp;lbrack;Warp&amp;rbrack;允許在視窗拖放時使用貼花模式來使用Alpha、材質和程序生成
* &amp;lbrack;投影&amp;rbrack;&amp;lbrack;Warp&amp;rbrack;使用帶有貼紙捷徑的曲速投影（ALT）
* &amp;lbrack;投影&amp;rbrack;&amp;lbrack;Warp&amp;rbrack;&amp;lbrack;Toolbar&amp;rbrack; 將warp作為整體或每個頂點轉換
* &amp;lbrack;投影&amp;rbrack;&amp;lbrack;Warp&amp;rbrack;&amp;lbrack;Toolbar&amp;rbrack; 新增格點，並可分割曲速，橫向、水平或垂直方向
* &amp;lbrack;Projection&amp;rbrack;&amp;lbrack;Warp&amp;rbrack;&amp;lbrack;Toolbar&amp;rbrack; 專用的重置動作選單
* &amp;lbrack;投影&amp;rbrack;&amp;lbrack;Warp&amp;rbrack;&amp;lbrack;Toolbar&amp;rbrack;移動點時自動調整切線的選項
* &amp;lbrack;投影&amp;rbrack;&amp;lbrack;Warp&amp;rbrack;&amp;lbrack;Toolbar&amp;rbrack;專用格線選單（大小、重置、顏色與握把大小）
* &amp;lbrack;投影&amp;rbrack;&amp;lbrack;Warp&amp;rbrack;新的鍵盤快捷鍵，可切換整個頂點的扭曲版模式（SHIFT+V）
* &amp;lbrack;投影&amp;rbrack;&amp;lbrack;Warp&amp;rbrack;點擊+Ctrl可切換表面工具與其他工具
* &amp;lbrack;投影&amp;rbrack;&amp;lbrack;圓柱形&amp;rbrack; 暴露圓柱投影模式
* &amp;lbrack;投影&amp;rbrack;&amp;lbrack;Toolbar&amp;rbrack;群組操作器設定（大小、格柵步進、角度步進）
* &amp;lbrack;色彩選擇器&amp;rbrack;新的色彩選擇器使用者介面
* &amp;lbrack;色彩選擇器&amp;rbrack;在色彩選擇器元件中使用 sRGB 值
* &amp;lbrack;Color Picker&amp;rbrack;允許儲存與刪除色片
* &amp;lbrack;色彩選擇器&amp;rbrack;滴管可從彩色及一般插槽操作
* &amp;lbrack;色彩選擇器&amp;rbrack;允許編輯 0 到 255 值之間的動態色彩
* &amp;lbrack;色彩選擇器&amp;rbrack;讓 HSV/RGB 狀態在整個應用程式中通用
* &amp;lbrack;Color Picker&amp;rbrack;Color Picker 視窗是半持久的
* &amp;lbrack;色彩選擇器&amp;rbrack;按下 Esc 鍵會關閉色彩選擇器視窗
* UI 互動及繪製時的效能提升
* &amp;lbrack;引擎&amp;rbrack;更新至新版 Substance 引擎（8.3.0）
* &amp;lbrack;腳本&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 允許重新載入目前專案的網格
* &amp;lbrack;腳本&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 允許更新專案中的資源
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 允許設定並查詢 UV 磚塊的解析度
* &amp;lbrack;互通性&amp;rbrack;不支援 Steam 和 Substance 版本
* &amp;lbrack;互通性&amp;rbrack;從橋接接收多重資源

**修正：**

* 色彩選擇器無法顯示正確的顏色
* &amp;lbrack;Baking&amp;rbrack;材質集合列表未正確排序
* &amp;lbrack;FBX 匯入&amp;rbrack;3ds Max 群組的樞紐轉換不被考慮
* &amp;lbrack;物質引擎&amp;rbrack;因進口損壞的SBSAR而墜毀
* &amp;lbrack;MacOS&amp;rbrack;不同語言的專案設定選項不存在
* 自動存檔可能會在長時間的過程中凍結 Painter

**已知問題：**

* &amp;lbrack;投影&amp;rbrack;&amp;lbrack;Warp&amp;rbrack;分割完成後仍保留分割選項
* &amp;lbrack;投影&amp;rbrack;&amp;lbrack;Warp&amp;rbrack; 當轉換設定為世界空間時，翻轉功能無法運作
* &amp;lbrack;投影&amp;rbrack;&amp;lbrack;Warp&amp;rbrack;在某些罕見情況下，補丁間的遺跡線條
* &amp;lbrack;投影&amp;rbrack;&amp;lbrack;UV&amp;rbrack; 翻轉投影時樞軸點會被重置
* &amp;lbrack;Mac M1&amp;rbrack;智慧材質無法正確顯示
* &amp;lbrack;M1&amp;rbrack;&amp;lbrack;Regression&amp;rbrack; 材料分層不正常

### 7.2.3

*（發布日期：2021*&#x200B;年8月24日）摘要： **小規模釋出，修正錯誤**

**補充：**

* &amp;lbrack;Libraries&amp;rbrack; 新增排除不想要檔案被抓取的方法

**修正：**

* &amp;lbrack;Win&amp;rbrack;多螢幕與睡眠問題
* &amp;lbrack;MacOS&amp;rbrack;&amp;lbrack;Crash&amp;rbrack; 使用效果時切換著色器
* &amp;lbrack;Viewport&amp;rbrack;完整預覽模式不再顯示無 alpha 的筆刷游標
* &amp;lbrack;UI&amp;rbrack;角度小工具轉錯方向
* &amp;lbrack;Layer Stack&amp;rbrack;許多子資料夾會造成非常長的凍結
* &amp;lbrack;Iray&amp;rbrack;Iray 與 OpenGL 中的不同視圖：若無法運作則可見
* &amp;lbrack;Iray&amp;rbrack;折射率不被考慮，且不會出現在 mdl 性質中
* &amp;lbrack;JavaScript&amp;rbrack; ShowExportDialog（） 從未回傳 true
* 無法從 Adobe Stock 讀取 MTL

### 7.2.2

*（發布日期：2021* 年 7 月 27 日）摘要： **小規模釋出，錯誤修正**

**補充：**

* 升級 AMD 驅動程式需求版本

**修正：**

* &amp;lbrack;Mac M1&amp;rbrack;錯誤記憶體偵測
* &amp;lbrack;出口&amp;rbrack;非常長的路徑無法正確顯示

**已知問題：**

* &amp;lbrack;內容&amp;rbrack;樣本的過時著色器

### 7.2.1

*（發布日期：2021*&#x200B;年7月2日）摘要： **小規模發行，熱修補**

**補充：**

* &amp;lbrack;Interop&amp;rbrack; 新增提示，告知尚未支援將 UV Tile 專案傳送至 Stager
* &amp;lbrack;Plugin&amp;rbrack;&amp;lbrack;UI&amp;rbrack; Livelink 圖示更新

**修正：**

* &amp;lbrack;Nvidia&amp;rbrack;驅動版本以 30 起被視為過時
* &amp;lbrack;Libraries&amp;rbrack;資產面板狀態除非專案開啟，否則不會被保存
* &amp;lbrack;Libraries&amp;rbrack; 新儲存搜尋保留舊儲存搜尋的關鍵字
* &amp;lbrack;Bakers&amp;rbrack;&amp;lbrack;UVTiles&amp;rbrack; 每個 meshID 的 ID 映射也會考慮 UV Tiles
* &amp;lbrack;Export&amp;rbrack;gLTF 檔案不會匯入頂點顏色
* &amp;lbrack;Iray&amp;rbrack;缺少一些提示
* &amp;lbrack;Interop&amp;rbrack;當未偵測到 Stager 時，傳送至 Stager 並不總是被停用
* &amp;lbrack;資源更新器&amp;rbrack;Photoshop 筆刷製作器無法更新
* &amp;lbrack;內容&amp;rbrack;玻璃纖維邊緣磨損發生器壞掉了

### 7.2.0

*（發布日期：2021* 年 6 月 23 日）摘要： **重大版本，新增資產面板、新增通道與參數的新著色器、整體介面更新、期待已久的效能提升、擴充語言支援等多項內容！**

**補充：**

* &amp;lbrack;圖書館&amp;rbrack;新資產面板以取代書架
* &amp;lbrack;Libraries&amp;rbrack;&amp;lbrack;UI&amp;rbrack;新資產面板佈局
* &amp;lbrack;Libraries&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 變更預設資產面板方向與使用者介面
* &amp;lbrack;Libraries&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 引入函式庫的列表檢視選項
* &amp;lbrack;Libraries&amp;rbrack\lbrack;UI&amp;rbrack;資產面板中的新麵包屑導航
* &amp;lbrack;Libraries&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 選擇已儲存搜尋時，選擇「所有資料庫」
* &amp;lbrack;Libraries&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 當所有資料夾取消選取時，選擇「所有函式庫」。
* &amp;lbrack;Libraries&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 粒子筆刷的新標籤
* &amp;lbrack;Libraries&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 在應用程式中將「shelf」替換為「All libraries」
* &amp;lbrack;Libraries&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 允許隱藏空資料夾
* &amp;lbrack;Libraries&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 預設使用者函式庫即使為空也應該可見
* &amp;lbrack;Libraries&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 透過資產類型圖示進行新的過濾方法
* &amp;lbrack;Libraries&amp;rbrack; 快捷鍵「CTRL」以選取多種資產類型
* &amp;lbrack;Libraries&amp;rbrack;新的環境變數用來控制資產預覽記憶體預算
* &amp;lbrack;Libraries&amp;rbrack;&amp;lbrack;Content&amp;rbrack; 新環境地圖
* &amp;lbrack;Libraries&amp;rbrack;&amp;lbrack;Content&amp;rbrack;&amp;lbrack;UI&amp;rbrack; Render displacement on default materials
* &amp;lbrack;Libraries&amp;rbrack;&amp;lbrack;Content&amp;rbrack; 設定 Adobe Standard Material （ASM） shader 作為預覽生成的預設
* &amp;lbrack;Libraries&amp;rbrack;&amp;lbrack;Content&amp;rbrack;&amp;lbrack;ASM&amp;rbrack; 新 ASM 著色器新專案範本
* &amp;lbrack;Libraries&amp;rbrack;&amp;lbrack;縮圖&amp;rbrack; 使用新的 Studio 6 環境映射
* &amp;lbrack;Libraries&amp;rbrack;&amp;lbrack;Thumbnail&amp;rbrack; 在資源中讀取縮圖，而非產生
* &amp;lbrack;Libraries&amp;rbrack;&amp;lbrack;縮圖&amp;rbrack; 在縮圖生成中加入位移
* &amp;lbrack;材質集設定&amp;rbrack;
* &amp;lbrack;紋理設定&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 向一般轉換方法顯示新高度
* &amp;lbrack;紋理集合設定&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 頻道介面組織的重製
* &amp;lbrack;紋理設定&amp;rbrack;使用者頻道限制提升至16頻道
* &amp;lbrack;紋理集設定&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 表示哪些通道與目前選擇的著色器相容
* &amp;lbrack;Shader&amp;rbrack;&amp;lbrack;ASM&amp;rbrack; 新 Adobe 標準材質著色器
* &amp;lbrack;Shader&amp;rbrack;&amp;lbrack;ASM&amp;rbrack;新增對各向異性、透明塗層、次表面散射、鏡面邊緣色彩及光澤的支援
* &amp;lbrack;Shader&amp;rbrack;&amp;lbrack;ASM&amp;rbrack; 變更預設通道的顏色值
* &amp;lbrack;Shader&amp;rbrack;&amp;lbrack;ASM&amp;rbrack;&amp;lbrack;Export&amp;rbrack; Updated export template Adobe Dimension to Adobe Substance 3D Stager
* &amp;lbrack;Shader&amp;rbrack;&amp;lbrack;ASM&amp;rbrack;新增著色器與 MDL 參數的標籤與工具提示
* &amp;lbrack;Shader&amp;rbrack;&amp;lbrack;ASM&amp;rbrack; 即使不支援 SSS，也讓散佈顏色在 2D 視圖中可見
* &amp;lbrack;Shader&amp;rbrack;&amp;lbrack;ASM&amp;rbrack;&amp;lbrack;Iray&amp;rbrack; 支援 Iray 中的 ASM 著色器，使用新的 MDL
* &amp;lbrack;Shader&amp;rbrack;&amp;lbrack;ASM&amp;rbrack;&amp;lbrack;Iray&amp;rbrack; 更新的舊式 PBR 規格光澤與塗層下的次表面散射
* &amp;lbrack;Shader&amp;rbrack;&amp;lbrack;ASM&amp;rbrack;&amp;lbrack;Content&amp;rbrack; 更改了樣本的預設 SSS 類型
* &amp;lbrack;Shader&amp;rbrack;&amp;lbrack;ASM&amp;rbrack; 新增 ASM API 文件
* &amp;lbrack;Shader&amp;rbrack;&amp;lbrack;ASM&amp;rbrack; 優化著色器以忽略未使用的通道
* &amp;lbrack;Shader&amp;rbrack;揭露新的貼圖集通道
* &amp;lbrack;著色器與 rbrack;改良的次表面散射
* &amp;lbrack;Shader&amp;rbrack;隱藏了部分著色器的新著色器參數
* &amp;lbrack;Shader&amp;rbrack;若用於著色器參數，則可見
* &amp;lbrack;Performance&amp;rbrack;
* &amp;lbrack;Libraries&amp;rbrack;資源預覽載入時間與計算效能提升
* &amp;lbrack;引擎與rbrack;塗裝性能改進
* &amp;lbrack;自動拆包&amp;rbrack;
* &amp;lbrack;自動拆包與拆包;包裝性能提升
* &amp;lbrack;自動展開&amp;rbrack;自動展開，與 UV Tile 工作流程相容
* &amp;lbrack;自動展開&amp;rbrack;新增根據網格方向定位 UV 的選項
* &amp;lbrack;其他&amp;rbrack;
* &amp;lbrack;設定&amp;rbrack; 更改預設縮放方向
* &amp;lbrack;UI&amp;rbrack;整體介面更新
* &amp;lbrack;UI&amp;rbrack;說明選單的重製
* &amp;lbrack;UI&amp;rbrack; 替換反轉圖示
* &amp;lbrack;UI&amp;rbrack;&amp;lbrack;Plugin&amp;rbrack; 替換插件 dcc 連結的圖示
* &amp;lbrack;UI&amp;rbrack;&amp;lbrack;AMD&amp;rbrack; 更新最低所需版本與彈出訊息
* &amp;lbrack;Layer Stack&amp;rbrack; 在選取的空資料夾內建立新圖層
* 更新 Python 文件
* &amp;lbrack;品牌&amp;rbrack;
* &amp;lbrack;Branding&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 應用程式名稱更新為 Adobe Substance 3D Painter
* &amp;lbrack;品牌設定&amp;rbrack;&amp;lbrack;UI&amp;rbrack;獨立版本更新為「Substance 版」
* &amp;lbrack;Branding&amp;rbrack;&amp;lbrack;UI&amp;rbrack;更新應用程式執行檔名稱、安裝路徑、套件與圖示
* &amp;lbrack;Branding&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 已重新命名預設函式庫與路徑
* &amp;lbrack;品牌設定&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 關於視窗的最新資訊
* &amp;lbrack;品牌設定&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 更新的歡迎畫面
* &amp;lbrack;品牌設定&amp;rbrack;&amp;lbrack;UI&amp;rbrack;移除基於年份的版本號
* &amp;lbrack;本地化&amp;rbrack;德文、法文及簡體中文的新翻譯
* &amp;lbrack;互通性&amp;rbrack;不支援 Steam 和 Substance 版本
* &amp;lbrack;互通性&amp;rbrack;與 Adobe 生態系統的互通性：Designer、Sampler、Stager 與 Bridge
* &amp;lbrack;互通性&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 從 Designer 接收並更新資產
* &amp;lbrack;互通性&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 從 Sampler 接收資產
* &amp;lbrack;互通性&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 將資產送給 Stager
* &amp;lbrack;互通性&amp;rbrack;&amp;lbrack;UI&amp;rbrack; Adobe Bridge 顯示
* &amp;lbrack;互通性&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 允許快速存取 Adobe 3D 資產
* &amp;lbrack;互通性&amp;rbrack;sbsar 的新使用標籤
* &amp;lbrack;互通性&amp;rbrack;處理接收資產類型
* &amp;lbrack;互通性&amp;rbrack;從 Adobe Substance 3D Designer 或 Adobe Substance 3D Sampler 收到的資產會儲存在使用者預設選擇的函式庫中
* &amp;lbrack;互通性&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 左側工具列新增圖示，可傳送給 Stager 或 Photoshop

**修正：**

* &amp;lbrack;Tablet&amp;rbrack;壓力噴漆時性能低
* &amp;lbrack;平板&amp;rbrack;滑桿控制平板上的問題
* &amp;lbrack;Crash&amp;rbrack;材質集合列表與匯出器名稱不符
* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Libraries&amp;rbrack; 雙擊子函式庫
* &amp;lbrack;Libraries&amp;rbrack; 爬取圖書館目錄時的問題
* &amp;lbrack;Libraries&amp;rbrack;強制預覽產生命令列無法如預期運作
* &amp;lbrack;Libraries&amp;rbrack;&amp;lbrack;Content&amp;rbrack; 烘焙光環境過濾器預設為黑色
* &amp;lbrack;Linux&amp;rbrack;&amp;lbrack;MacOS&amp;rbrack;&amp;lbrack;Export Mesh&amp;rbrack; 無法匯入在 Linux/MacOS 上創建的 glTF
* &amp;lbrack;Linux&amp;rbrack;拖放檔案到資產面板可能會導致當機
* &amp;lbrack;自動展開&amp;rbrack;即使未選擇網格重新載入，自動展開功能仍可用
* &amp;lbrack;粒子&amp;rbrack;粒子與重力的錯誤行為
* &amp;lbrack;Layer Stack&amp;rbrack;Level 直方圖只能在某些通道中使用亮度
* &amp;lbrack;幾何遮罩&amp;rbrack;當編輯幾何遮罩時，右鍵點擊資料夾選單無法運作
* &amp;lbrack;投影與雙線性濾波的縫隙;
* &amp;lbrack;UV Tiles&amp;rbrack; 匯出遮罩到檔案只輸出圖塊 0， 0
* &amp;lbrack;Export Mesh&amp;rbrack;FBX 網格匯出為空
* &amp;lbrack;Iray&amp;rbrack;新專案渲染時不會考慮法線貼圖
* &amp;lbrack;Save&amp;rbrack;共享磁碟上的存檔問題
* &amp;lbrack;Baking&amp;rbrack;重新烘焙時會顯示警告
* &amp;lbrack;Baking&amp;rbrack;&amp;lbrack;Regression&amp;rbrack; 當高多邊形網格的全域包圍框未包含場景原點時，結果錯誤
* &amp;lbrack;Python&amp;rbrack;自訂使用者函式庫不被考慮

**已知問題：**

* &amp;lbrack;Libraries&amp;rbrack;若未開啟專案，則未儲存的搜尋
* &amp;lbrack;NVIDIA&amp;rbrack;即使驅動程式是最新的，仍會收到過時驅動的訊息

### 7.1.1 (2021.1.1)

*（發布日期：2021* 年 3 月 23 日）摘要： **小規模釋出，修正錯誤，並可於色彩選擇器中輸入十六進位數值**

**補充：**

* &amp;lbrack;Log&amp;rbrack;提醒使用者注意不相容的 AMD GPU 驅動程式
* &amp;lbrack;Color Picker&amp;rbrack;允許輸入十六進位值

**修正：**

* &amp;lbrack;Baker&amp;rbrack;表現下滑
* &amp;lbrack;Geometry mask&amp;rbrack;Alt 點擊網格名稱可能會導致當機
* &amp;lbrack;Engine&amp;rbrack;繪圖在必要時不會刷新整個視圖
* &amp;lbrack;Layer stack&amp;rbrack;切換著色器後選擇卡住
* &amp;lbrack;MacOS&amp;rbrack;&amp;lbrack;Color picker&amp;rbrack;顏色與被選取的略有不同
* &amp;lbrack;Export&amp;rbrack;使用 PSD 檔案格式不會在每個 UV 圖塊產生一個檔案
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Javascript&amp;rbrack; alg.mapexport.getPathsExportDocumentMaps（） 不會回傳所有值
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack;重新開啟 Painter 時，停用的外掛會再次啟用

### 7.1.0 (2021.1.0)

*（發布日期：2021* 年 1 月 28 日）摘要： **重大版本，新增 Geometry Mask，允許選取並繪製幾何體部分，圖層堆疊中複製/貼上效果，改進 UV 圖塊工作流程，更新 Iray、Bakers、Substance Engine 及新增內容**

**補充：**

* 新的幾何遮罩，並繪製選取的幾何部分
* &amp;lbrack;幾何遮罩&amp;rbrack;允許以網格名稱繪製幾何體的部分
* &amp;lbrack;幾何遮罩&amp;rbrack;兩個視窗中的矩形選擇
* &amp;lbrack;幾何遮罩&amp;rbrack;允許隱藏/忽略任何圖層中被排除的幾何體
* &amp;lbrack;幾何遮罩&amp;rbrack;&amp;lbrack;Properties&amp;rbrack; 快速選取勾選框，點擊拖曳即可
* &amp;lbrack;幾何遮罩&amp;rbrack;&amp;lbrack;Properties&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 在屬性視窗中加入/排除所有物件，使用下拉選單
* &amp;lbrack;幾何掩罩&amp;rbrack;&amp;lbrack;Properties&amp;rbrack; 允許以 ALT+LEFT Click 快速選取列表中的一個項目
* &amp;lbrack;Geometry Mask&amp;rbrack;&amp;lbrack;Properties&amp;rbrack; 在視口中，當滑鼠滑鼠在屬性視窗中 Mesh 名稱/UV Tiles 時的覆蓋層
* &amp;lbrack;幾何遮罩&amp;rbrack;&amp;lbrack;層疊疊&amp;rbrack;為幾何遮罩新增複製/貼上選項
* &amp;lbrack;幾何遮罩&amp;rbrack;隱藏/忽略排除幾何按鈕的新圖示
* &amp;lbrack;幾何遮罩&amp;rbrack;隱藏/忽略排除幾何體的新提示
* &amp;lbrack;幾何遮罩&amp;rbrack;鍵盤快捷鍵 ALT+H 可切換「隱藏 忽略排除幾何」按鈕
* &amp;lbrack;UV Tiles&amp;rbrack;&amp;lbrack;Layer Stack&amp;rbrack; 新填充圖層球體預覽縮圖，適用於 UV Tiles 與簡化模式
* &amp;lbrack;UV Tiles&amp;rbrack;&amp;lbrack;Layer Stack&amp;rbrack; 允許輕鬆退出 UV Tile 遮罩
* &amp;lbrack;UV Tiles&amp;rbrack;&amp;lbrack;Texture Set List&amp;rbrack; 允許為每個 UV 圖塊提供描述
* &amp;lbrack;UV Tiles&amp;rbrack;&amp;lbrack;Texture Set Settings&amp;rbrack;&amp;lbrack;UI&amp;rbrack;下拉選單新增兩個區塊標題，用來更改 UV 圖塊解析度
* &amp;lbrack;UV Tiles&amp;rbrack;&amp;lbrack;Viewport&amp;rbrack; 拖曳材質進入視窗時，退出 UV 圖塊遮罩
* &amp;lbrack;疊加 Stack&amp;rbrack; 新增效果的複製/貼上選項
* &amp;lbrack;Layer Stack&amp;rbrack; 允許將效果從一個材質集複製/貼上到另一個
* &amp;lbrack;Layer Stack&amp;rbrack;允許多重選擇效果
* &amp;lbrack;Layer Stack&amp;rbrack;新增複製/貼上選項作為圖層效果的快捷鍵
* &amp;lbrack;Layer Stack&amp;rbrack;拖曳效果到另一圖層時，會自動在遮罩與內容之間切換
* &amp;lbrack;Layer Stack&amp;rbrack;貼上其他圖層遮罩時自動建立遮罩
* &amp;lbrack;Layer Stack&amp;rbrack; 在效果的情境右鍵選單中新增移動效果動作
* &amp;lbrack;Layer Stack&amp;rbrack;允許將效果從一層拖到另一層
* &amp;lbrack;疊加 堆疊&amp;rbrack;將項目拖曳到資料夾上，會將它們置於資料夾頂端
* 更新 Iray 至 2020.1.0 版本
* &amp;lbrack;Bakers&amp;rbrack;更新 Bakers 至 2.5.4 版本
* &amp;lbrack;Bakers&amp;rbrack;在烘焙進度視窗中顯示個別 UV 磚塊
* &amp;lbrack;Bakers&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 允許用新按鈕快速烘焙目前的貼圖集
* &amp;lbrack;Bakers&amp;rbrack;允許使用者透過 Alt+LEFT 點擊快速選取其中一位烘焙師
* 更新 Substance Engine 至 8.0.8 版本
* &amp;lbrack;Substance Engine &amp;rbrack; 支援新 .sbsar 檔案中的預設顏色
* &amp;lbrack;自動展開&amp;rbrack;性能提升
* &amp;lbrack;Export&amp;rbrack; 新增視覺回饋，以標示哪個 UV 圖塊的解析度與專案預設不同
* &amp;lbrack;Export&amp;rbrack;將場景大小因子加入匯出後的著色器 JSON 檔案
* &amp;lbrack;語言&amp;rbrack;新增日文翻譯
* &amp;lbrack;UI&amp;rbrack; 關於具有內部相依版本控制的視窗更新
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 允許管理架上資源
* &amp;lbrack;腳本&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 允許知道專案何時準備好烘焙與匯出
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 允許知道 Shelf 何時完成在磁碟上的資源爬取
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 允許查詢每個貼圖集的 UV 圖塊列表
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 允許將自訂預覽分配到 Shelf 資源
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 允許管理自訂書架
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 在文件中的每個子模組中新增方法索引
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 文件的新風格
* &amp;lbrack;腳本&amp;rbrack;&amp;lbrack;Python&amp;rbrack;資源與 Shelf 文件的改進
* &amp;lbrack;內容&amp;rbrack;三個新的工具預設，用於製作針法
* &amp;lbrack;Shelf&amp;rbrack;在過渡到新的Substance Share平台時，暫時移除「Export to Substance Share」

**修正：**

* 使用不同解析度的螢幕時會當機
* Substance Engine 的崩潰與一些罕見專案
* 切換圖層時，視窗刷新會因隱藏/忽略排除幾何而失敗
* &amp;lbrack;2D View&amp;rbrack;有些專案可能缺少 2D Viewport
* &amp;lbrack;Baking&amp;rbrack;「依網格名稱匹配」會忽略物件的部分
* &amp;lbrack;Layer Stack&amp;rbrack;點擊圖層效果會開啟資料夾
* &amp;lbrack;幾何遮罩&amp;rbrack;即使重新匯入網格且沒有遮罩，UV 圖塊仍會被計入遮罩
* &amp;lbrack;幾何遮罩&amp;rbrack;視窗中的右鍵選單無法提供正確的工具
* &amp;lbrack;引擎與rbrack;在特定專案上嚴重延遲
* &amp;lbrack;Scripting&amp;rbrack;在 Windows 上遠端 JSON POST 請求時，高延遲
* &amp;lbrack;Linux&amp;rbrack;特定整合顯示卡無法正確偵測 Vram 容量
* &amp;lbrack;自動展開&amp;rbrack;某些專案會崩潰或展開時間過長

## 版本 6

### 6.2.2 (2020.2.2)

*（發布日期：2020* 年 9 月 28 日）摘要： **次要版本，包含部分 Python API 函式的錯誤修正**

**補充：**

* &amp;lbrack;Performance&amp;rbrack;使用色彩 ID 選擇時，請不要計算所有 UV 磚塊
* &amp;lbrack;Bakers&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 顯示材質集描述
* &amp;lbrack;Bakers&amp;rbrack; 允許儲存烘焙設定
* &amp;lbrack;Bakers&amp;rbrack; 新增全部摺疊/展開所有選項至選擇標籤
* &amp;lbrack;材質集合列表&amp;rbrack;空時隱藏描述
* &amp;lbrack;UV Tiles&amp;rbrack;&amp;lbrack;Texture Set List&amp;rbrack; 點擊 UV Tile 應該會展開或摺疊列表
* &amp;lbrack;Export&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 允許水平調整貼圖集清單面板大小
* &amp;lbrack;Export&amp;rbrack;&amp;lbrack;UI&amp;rbrack;UV Tiles 與 Texture Set 工作流程（未選取材質）的一致提示文字
* &amp;lbrack;腳本&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 允許使用匯出預設來匯出貼圖
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 在文件中新增變更日誌
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 允許查詢給定堆疊上所有可用通道
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 控制台介面改進

**修正：**

* &amp;lbrack;AMD&amp;rbrack;錯誤偵測過時驅動版本
* 在某些情況下，重新匯入帶有不同 UV Tiles 佈局的網格時會當機
* 在非常重的網格上使用帶有 UDIM 的粒子時會當機
* &amp;lbrack;UV Tiles&amp;rbrack;在某些情況下匯出帶有位移資訊的網格時會當機
* &amp;lbrack;Export&amp;rbrack;&amp;lbrack;Crash&amp;rbrack; 將 2D 視圖匯出成 psd 格式可能會導致當機
* 在建立專案時將圖片匯入為序列無法運作
* 引擎陷入無盡的循環
* &amp;lbrack;Shortcut&amp;rbrack;切換快遞模式捷徑時，鏡頭總是以 snap 模式旋轉
* 即使選項關閉，網格重新匯入時也會自動展開
* &amp;lbrack;紋理集合列表&amp;rbrack;描述文字欄位在版本中有時不會完全顯示
* &amp;lbrack;材質集合清單&amp;rbrack;用來隱藏或解除隱藏材質集的下拉選單無法完全顯示
* &amp;lbrack;Texture Set List&amp;rbrack;點擊眼睛圖示不應輸入「編輯材質集名稱」
* &amp;lbrack;Texture Set Settings&amp;rbrack;移除通道也會移除下面的通道
* &amp;lbrack;Export&amp;rbrack;包含所有並重置所有，並未考慮 UV 圖塊
* &amp;lbrack;Bakers&amp;rbrack;被淘汰的烘焙師會出現在烘焙過程中
* 解析度更新不會計入用於輸入的烘焙地圖
* &amp;lbrack;UV Tiles&amp;rbrack;&amp;lbrack;Viewport&amp;rbrack; 在選擇 UV Tile 遮罩後加入 Smart Material 後，3D 視窗凍結
* &amp;lbrack;UV Tiles&amp;rbrack;&amp;lbrack;Viewport&amp;rbrack; 線框對於隱藏圖塊，透過繪畫模式仍然可見
* &amp;lbrack;Export&amp;rbrack;&amp;lbrack;Sketchfab&amp;rbrack;「plus」訂閱類型的問題
* &amp;lbrack;Sketchfab&amp;rbrack;「此資產為私人資產」勾選框在更換帳號後不會顯示
* &amp;lbrack;Export&amp;rbrack;&amp;lbrack;內容&amp;rbrack;「Wiggly」筆刷預設可能導致效能問題
* &amp;lbrack;Plugin Photoshop&amp;rbrack;日誌訊息：與 UV Tile 工作流程不相容
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; PYTHONPATH env var 阻止應用程式啟動
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; Python documentation 中的打字錯誤

### 6.2.1 (2020.2.1)

*（發布日期：2020* 年 7 月 29 日）摘要： **小規模釋出，熱修補**

**補充：**

* 新增環境變數「SUBSTANCE_PAINTER_VRAM_BUDGET」來覆蓋 GPU VRam 數量
* &amp;lbrack;UV 圖塊&amp;rbrack;&amp;lbrack;Performance&amp;rbrack; 使用多邊形填充工具時，請不要計算所有 UV 圖塊

**修正：**

* &amp;lbrack;Iray&amp;rbrack; 儲存渲染會回傳錯誤，導致畫面呈現黑色
* &amp;lbrack;Linux&amp;rbrack;在 CentOS 7.3 開機畫面後當機
* &amp;lbrack;Linux&amp;rbrack;特定設定下無法正確偵測到 Vram 容量
* &amp;lbrack;Crash&amp;rbrack;開啟一個帶有重複材質集名稱的專案
* &amp;lbrack;Engine&amp;rbrack; 修改遮罩時快取失效問題
* &amp;lbrack;紋理集合列表&amp;rbrack;當貼圖集停用時出現錯誤字型效果

**已知問題：**

* &amp;lbrack;貼圖集合列表&amp;rbrack;無法隱藏描述
* &amp;lbrack;貼圖集合列表&amp;rbrack;UI 問題
* &amp;lbrack;Iray&amp;rbrack;PSD 渲染無法開啟
* &amp;lbrack;插件 Photoshop&amp;rbrack;不相容於 UV Tiles 工作流程

### 6.2.0 (2020.2.0)

*（發布日期：2020* 年 7 月 23 日）摘要： **重大釋出，新增 UV 磚塊工作流程、跨 UV 磚塊繪圖及效能提升**

**補充：**

* UV 瓷磚（UDIM 系統）
* &amp;lbrack;UV 磁磚 &amp;rbrack; 在 UV 磁磚上繪製
* &amp;lbrack;UV Tiles&amp;rbrack;允許在 UV Tiles 的新與舊工作流程間選擇
* &amp;lbrack;UV Tiles&amp;rbrack; 將 UDIM 或 UV Tile 影像序列匯入為資源
* &amp;lbrack;UV Tiles&amp;rbrack; 在貼圖集列表視窗中為每個材質集新增 UV 磚塊清單
* &amp;lbrack;UV Tiles&amp;rbrack; 允許在貼圖集設定中同時編輯多個 UV Tiles 的解析度
* &amp;lbrack;UV 圖塊&amp;rbrack;&amp;lbrack;2D View&amp;rbrack; 以格子形式顯示 UV 圖塊
* &amp;lbrack;UV Tiles&amp;rbrack;&amp;lbrack;2D View&amp;rbrack; 新的視窗按鈕用以顯示或隱藏 UV Tiles 資訊
* &amp;lbrack;UV Tiles&amp;rbrack; 預設為 UV 圖塊專案的繪製工具切換為單通道
* &amp;lbrack;UV Tiles&amp;rbrack;在情境工具列新增按鈕，可以在繪製時忽略遮罩的 UV Tiles
* &amp;lbrack;UV Tiles&amp;rbrack;&amp;lbrack;Layer Stack&amp;rbrack;新增圖層堆疊圖示以提升效能
* &amp;lbrack;UV Tiles&amp;rbrack;&amp;lbrack;Layer Stack&amp;rbrack;改善工具列中的繪圖與填充圖示
* &amp;lbrack;UV 圖塊遮罩&amp;rbrack;&amp;lbrack;2D View&amp;rbrack; 允許同時包含或排除多個 UV 圖塊（左鍵點擊，CTRL+左鍵點擊）
* &amp;lbrack;UV 圖塊遮罩&amp;rbrack;新增 UV 圖塊遮罩，並以新圖示排除每層圖騰的圖塊
* &amp;lbrack;UV Tile Mask&amp;rbrack\lbrack;Layer Stack&amp;rbrack; 當 UV Tiles 遮罩圖示中未包含所有 UV 圖塊時，顯示 UV 圖塊的數量
* &amp;lbrack;UV 圖塊遮罩&amp;rbrack;&amp;lbrack;2D/3D View&amp;rbrack; 新增懸浮效果以視覺化游標下方的 UV 圖塊
* &amp;lbrack;UV 磚塊&amp;rbrack;&amp;lbrack;Bakers&amp;rbrack; 允許選擇並烘焙特定的 UV 磚塊
* &amp;lbrack;UV 磚塊&amp;rbrack;&amp;lbrack;Bakers&amp;rbrack; 新增紋理集/UV 磚塊的選擇選項
* &amp;lbrack;UV Tiles&amp;rbrack;&amp;lbrack;Bakers&amp;rbrack; 右鍵選單選項，選擇材質集內的 UV Tiles
* &amp;lbrack;UV Tiles&amp;rbrack;&amp;lbrack;Bakers&amp;rbrack; 允許在材質集/UV Tiles 中拖曳快速選取
* &amp;lbrack;UV Tiles&amp;rbrack;&amp;lbrack;Bakers&amp;rbrack; 將網格地圖中的「全部」和「無」按鈕替換成更明確的選擇選項
* &amp;lbrack;UV Tiles&amp;rbrack;&amp;lbrack;Bakers&amp;rbrack; 顯示待烘焙的貼圖數量
* &amp;lbrack;UV 磚塊&amp;rbrack;&amp;lbrack;Export&amp;rbrack; 允許選擇並匯出特定 UV 磚塊
* &amp;lbrack;UV 磚塊&amp;rbrack;&amp;lbrack;Export&amp;rbrack; 透過拖曳快速選擇 UV 磚塊
* &amp;lbrack;UV 磚塊&amp;rbrack;&amp;lbrack;Export&amp;rbrack; 新增 UV 磚塊的下拉選單選項
* &amp;lbrack;UV Tiles&amp;rbrack;&amp;lbrack;Export&amp;rbrack; 如果某些匯出預設不支援 UV Tiles（Adobe Dimension、Sketchfab、glTF、USD），請將其無法使用。
* &amp;lbrack;UV Tiles&amp;rbrack;&amp;lbrack;Content&amp;rbrack; 更新匯出預設以使用新的 $udim 標籤
* &amp;lbrack;UV Tiles&amp;rbrack;在匯入帶有重疊 UV 島嶼的網格時，改善錯誤報告
* &amp;lbrack;UV 磚塊&amp;rbrack;與 Iray 相容的 UV 磚塊
* &amp;lbrack;UV Tiles&amp;rbrack;&amp;lbrack;Scripting&amp;rbrack; Add UV Tile export documentation 到 Python doc
* 性能
* &amp;lbrack;Performance&amp;rbrack;情境工具列新增按鈕，工作時可暫停引擎運算（SHIFT+ESC）
* &amp;lbrack;Performance&amp;rbrack;透過延遲紋理集快取計算來加速專案開啟
* &amp;lbrack;Performance&amp;rbrack; 開啟專案時不要等網格貼圖載入
* &amp;lbrack;Performance&amp;rbrack;&amp;lbrack;2D/3D View&amp;rbrack; 當 Mask 通道未被使用時，請勿在視窗中計算
* &amp;lbrack;Performance&amp;rbrack;載入視窗中顯示的網格貼圖時，請勿阻塞應用程式
* &amp;lbrack;Performance&amp;rbrack;在儲存專案時提升增量儲存速度
* &amp;lbrack;Performance&amp;rbrack;&amp;lbrack;Bakers&amp;rbrack; 更改預設膨脹設定以提升節省時間與專案規模
* &amp;lbrack;Performance&amp;rbrack;&amp;lbrack;Bakers&amp;rbrack; 在特定烘焙機上切換至灰階，以節省時間並提升專案規模
* &amp;lbrack;性能&amp;rbrack;&amp;lbrack;Export&amp;rbrack; 提升引擎效能以更快匯出貼圖
* &amp;lbrack;Performance&amp;rbrack;&amp;lbrack;Export&amp;rbrack; 在開啟大量材質集的匯出對話框時，提升反應速度
* &amp;lbrack;Performance&amp;rbrack;&amp;lbrack;Export&amp;rbrack; 切換到「List of Exports」分頁時提升效能
* &amp;lbrack;Performance&amp;rbrack;&amp;lbrack;Iray&amp;rbrack; 減少 Iray 啟動時間
* 其他
* &amp;lbrack;Bakers&amp;rbrack; 新增材質集的選擇選項
* 將著色器實例管理移至貼圖集設定
* &amp;lbrack;2D/3D View&amp;rbrack;在視窗底部新增訊息，指示被編輯的遮罩類型
* &amp;lbrack;疊加堆疊&amp;rbrack;設定中新增選項，可在舊有縮圖與新縮圖間切換
* &amp;lbrack;疊加 Stack&amp;rbrack;新增視覺回饋以指示縮圖的載入狀態
* &amp;lbrack;Proj&amp;rbrack;新增投影模式「Fill （Match Per UV-Tile）」以載入影像序列
* &amp;lbrack;Proj&amp;rbrack;在特定情況下將填充圖層投影模式改為「填充（逐 UV 圖塊匹配）」
* &amp;lbrack;內容&amp;rbrack;優化 Charcoal 筆刷預設以提升效能
* 更新 Iray 至 2020.0.0 版本
* &amp;lbrack;Export&amp;rbrack;當沒有選擇時，停用匯出清單標籤
* 自動展開
* &amp;lbrack;自動展開&amp;rbrack;提升自動展開流程的成功率
* &amp;lbrack;自動展開&amp;rbrack;改良參數化以提升速度與穩定性

**修正：**

* &amp;lbrack;Alembic&amp;rbrack;匯入檔案時忽略面板集
* &amp;lbrack;Alembic&amp;rbrack;特定檔案的無限載入時間
* &amp;lbrack;Import&amp;rbrack;當僅檔案副檔名不同時，匯入錯誤的 UDIM 影像序列
* &amp;lbrack;Crash&amp;rbrack; 嘗試開啟被其他程序鎖定的專案會導致當機
* &amp;lbrack;投影&amp;rbrack;使用三平面投影時，複製網格上的瑕疵
* &amp;lbrack;Export&amp;rbrack;發射通道不會以美元格式匯出
* &amp;lbrack;內容&amp;rbrack; 智慧材質「炭筆」包含繪畫筆觸

**已知問題：**

* &amp;lbrack;貼圖集合列表&amp;rbrack;無法隱藏描述
* &amp;lbrack;貼圖集合列表&amp;rbrack;UI 問題

### 6.1.3 (2020.1.3)

*（發布日期：2020* 年 6 月 16 日）摘要： **錯誤修正**

**補充：**

* &amp;lbrack;Export&amp;rbrack; 在 Shader 參數 json 檔案中新增位移設定

**修正：**

* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Engine&amp;rbrack; 嘗試清除並替換現有通道時會當機
* &amp;lbrack;Crash&amp;rbrack; 在材質層疊繪遮罩後更換著色器
* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Engine&amp;rbrack;與一些重項目一起墜毀
* &amp;lbrack;Bakers&amp;rbrack;以名字匹配無法與從 zBrush 匯出的 OBJ 相符
* &amp;lbrack;Displacement&amp;rbrack;&amp;lbrack;SVT&amp;rbrack; 當置換開啟時，貼圖不會在專案開啟時顯示
* &amp;lbrack;Export&amp;rbrack;有些材質會匯出為均勻灰色
* &amp;lbrack;Export&amp;rbrack;停用的材質集不應匯出用於 Dimension 和 Sketchfab 匯出預設
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;JavaScript&amp;rbrack;使用 JavaScript API 存取 onProjectOpened 事件中的匯出設定時當機
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Javascript&amp;rbrack; onExportFinished（） 不會在匯出後呼叫

### 6.1.2 (2020.1.2)

*（發布日期：2020* 年 5 月 28 日）摘要： **Substance Engine 與 Bakers 更新的錯誤修正**

**補充：**

* &amp;lbrack;Bakers&amp;rbrack;更新至最新版本
* &amp;lbrack;Bakers&amp;rbrack; 環境遮蔽、曲率、厚度烘焙機的新取樣方法
* 最新版本的Substance Engine更新
* &amp;lbrack;腳本&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 允許為專案資源建立 ResourceID
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 允許查詢通道資訊
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; 加入試演與回調函式以模擬材質匯出

**修正：**

* &amp;lbrack;Bakers&amp;rbrack;世界空間法線中錯誤的法線 Baker 在特定情況下使用切線法線貼圖
* &amp;lbrack;Bakers&amp;rbrack;在沒有高多邊形時，使用 Optix 烘焙環境遮蔽時出現錯誤
* &amp;lbrack;動態筆觸&amp;rbrack;載入特定材質集時會延遲
* &amp;lbrack;Export&amp;rbrack;不應該匯出已停用的美金材質集，glTF
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;JavaScript&amp;rbrack; 無法編輯新的 Curvature Baker 設定
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;JavaScript&amp;rbrack; alg.texturesets.addChannel（） 在某些情況下不會回傳錯誤
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;JavaScript&amp;rbrack; Typo in Javascript API documentation for setProjectExportOptions（）
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;JavaScript&amp;rbrack; 總是匯出所有材質集
* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;Python&amp;rbrack; sys.executable 會回傳路徑到 python.exe 而非 Substance Painter
* 紋理快取在 Mac OS 與 Windows/Linux 間不相容
* &amp;lbrack;Livelink UE4&amp;rbrack;合併網格中所有材質集只使用最後材質

**已知問題：**

* &amp;lbrack;Export&amp;rbrack;&amp;lbrack;Dimension&amp;rbrack;&amp;lbrack;Skecthfab&amp;rbrack; 不應匯出已停用的材質集
* &amp;lbrack;Crash&amp;rbrack;在材質層疊後更換遮罩

### 6.1.1 (2020.1.1)

*（發布日期：2020* 年 5 月 5 日）摘要： **熱修正**

**補充：**

* &amp;lbrack;Export&amp;rbrack;在 TextureSet 上被覆寫狀態的視覺回饋

**修正：**

* &amp;lbrack;Export&amp;rbrack;匯出器視窗在特殊解析度螢幕上過大，無法調整大小
* &amp;lbrack;Export&amp;rbrack;匯出後選項不會被儲存
* &amp;lbrack;Export&amp;rbrack;當機或無法用「從快取」匯出預設匯出
* &amp;lbrack;Export&amp;rbrack;取消輸出會產生一個意外的額外空白地圖
* &amp;lbrack;Export&amp;rbrack; 修正虛擬匯出預設設定
* &amp;lbrack;Python&amp;rbrack; PYTHONPATH env var 不被考慮
* &amp;lbrack;Python&amp;rbrack;&amp;lbrack;Export&amp;rbrack; 透過 Python 取消匯出會回傳異常錯誤
* &amp;lbrack;Python&amp;rbrack;&amp;lbrack;Export&amp;rbrack; export_project_textures PSD 檔案格式的結果錯誤
* &amp;lbrack;Bakers&amp;rbrack;在 Linux 上使用 GPU 光線追蹤時當機

**已知問題：**

* &amp;lbrack;JavaScript&amp;rbrack;無法編輯新的 Curvature 烘焙器設定
* &amp;lbrack;JavaScript&amp;rbrack;&amp;lbrack;Export&amp;rbrack; 總是匯出所有材質集
* &amp;lbrack;Export&amp;rbrack;&amp;lbrack;USD&amp;rbrack; 不應匯出已停用的材質集
* &amp;lbrack;Crash&amp;rbrack;在材質層疊後更換遮罩

### 6.1.0 (2020.1.0)

*（發布日期：2020* 年 4 月 22 日）摘要： **重大版本推出，新增貼圖與網格匯出器（包含位移與細分）、更新的 UV 展開並加入更多控制項、新烘焙工具、新的腳本 Python API、更佳的貼花投影用戶體驗及新內容**

**補充：**

* 新的貼圖與網格匯出器
* &amp;lbrack;Export&amp;rbrack; 新匯出介面
* &amp;lbrack;Export&amp;rbrack;&amp;lbrack;Export tab&amp;rbrack; 允許選擇每個材質集匯出哪些地圖頻道
* &amp;lbrack;Export&amp;rbrack;&amp;lbrack;Export tab&amp;rbrack; 允許一次操作修改所有材質集的貼圖集大小
* &amp;lbrack;Export&amp;rbrack;&amp;lbrack;Export tab&amp;rbrack;允許每個材質集使用不同的模板（除了 USD、glTF、Sketchfab 和 Dimension）
* &amp;lbrack;Export&amp;rbrack;&amp;lbrack;Export tab&amp;rbrack;快速啟動與停用貼圖與材質集
* &amp;lbrack;Export&amp;rbrack;&amp;lbrack;Export tab&amp;rbrack;匯出解析度 8192x8192 不再實驗性
* &amp;lbrack;Export&amp;rbrack;&amp;lbrack;Export tab&amp;rbrack;允許修改檔案格式及每張地圖的位元深度
* &amp;lbrack;Export&amp;rbrack;&amp;lbrack;Export tab&amp;rbrack; 允許重設為預設參數值
* &amp;lbrack;Export&amp;rbrack;&amp;lbrack;Export tab&amp;rbrack; 允許設定儲存而不必匯出
* &amp;lbrack;Export&amp;rbrack;&amp;lbrack;Output templates tab&amp;rbrack; 將「Configuration」分頁改名為「Output templates」分頁
* &amp;lbrack;Export&amp;rbrack;&amp;lbrack;輸出模板 tab&amp;rbrack;允許定義每個預設映射的檔案格式與位元深度
* &amp;lbrack;Export&amp;rbrack;&amp;lbrack;List of exports tab&amp;rbrack; 新預覽標籤，用於摘要與檢視匯出流程
* &amp;lbrack;Import/Export Mesh&amp;rbrack;Import/Export 時間效能優化
* &amp;lbrack;匯出網格&amp;rbrack;在FBX中匯出網格
* &amp;lbrack;匯出網格&amp;rbrack;匯出帶有位移與鑲嵌的網格
* &amp;lbrack;Export Mesh&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 重新計算正常頂點的新設定，應用三角測量
* &amp;lbrack;匯出網格&amp;rbrack;匯出原始網格拓撲，並由自動展開產生新UV
* 更新了自動 UV 展開，新增了更多控制項
* &amp;lbrack;UV 展開&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 新增設定以在新專案視窗中啟用自動 UV 展開
* &amp;lbrack;UV 展開&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 控制展開步驟的新選項（縫線、展開、包裝）
* &amp;lbrack;UV 展開&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 允許保留現有展開接縫/展開/包裝
* &amp;lbrack;UV 展開&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 全新選項可完全重新計算展開步驟
* &amp;lbrack;UV 展開&amp;rbrack;&amp;lbrack;UI&amp;rbrack;新選項可控制邊距大小（無、小、中、大）
* 新麵包師
* &amp;lbrack;Bakers&amp;rbrack;將舊的曲率換成網狀的新曲率
* &amp;lbrack;Bakers&amp;rbrack; 新增以名稱匹配的選項，以忽略「環境遮蔽」烘焙機中的背面
* &amp;lbrack;Bakers&amp;rbrack; 在「環境遮蔽」烘焙機中新增接地平面選項
* 新腳本 Python API（3.7.6）
* &amp;lbrack;Python&amp;rbrack;&amp;lbrack;UI&amp;rbrack; Python 新腳本選單
* &amp;lbrack;Python&amp;rbrack;&amp;lbrack;UI&amp;rbrack;新 Python 文件於說明選單中
* &amp;lbrack;Python&amp;rbrack; Expose Substance Painter Python 模組：substance_painter、alg、display、project.setting、project、texturesets、ui
* &amp;lbrack;Python&amp;rbrack; 公開新的「substance_painter」Python 模組
* &amp;lbrack;Python&amp;rbrack;公開新的 Python 子模組：alg、display、log、project、resource、textureset、ui
* &amp;lbrack;Python&amp;rbrack; 專案變更的監聽器
* &amp;lbrack;Python&amp;rbrack;Python 文件中的新範例
* &amp;lbrack;JavaScript&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 插件選單被 JavaScript 取代
* &amp;lbrack;Viewport&amp;rbrack;允許透過「拖放+ALT」從書架上擷取資源來建立貼花投影
* 新內容
* &amp;lbrack;內容&amp;rbrack;來自Substance Source的5種新貼紙材料
* &amp;lbrack;內容&amp;rbrack; 新增專案範本並匯出 Maxwell 渲染器的預設
* &amp;lbrack;內容&amp;rbrack; 新增 Keyshot 9 匯出專案模板
* &amp;lbrack;Content&amp;rbrack;更新 Keyshot 9 匯出預設以支援位移與發射
* &amp;lbrack;內容&amp;rbrack;&amp;lbrack;Exporter&amp;rbrack; 更新所有匯出預設以符合最新遊戲引擎與渲染器版本
* &amp;lbrack;內容&amp;rbrack;&amp;lbrack;Exporter&amp;rbrack; 更新匯出預設檔以使用新的格式與抖動設定
* &amp;lbrack;內容&amp;rbrack;支援 VRay 材質的新模板與著色器（VRayMtl）
* &amp;lbrack;Layer Stack&amp;rbrack;允許使用垃圾圖示或鍵盤快捷鍵刪除圖層效果 刪除
* 移除 Substance Source 插件（使用具備「傳送」功能的啟動器）
* &amp;lbrack;Windows&amp;rbrack;高階 GPU 上不顯示 TDR 警告

**修正：**

* 新專案檔案對話框中的翻譯問題
* &amp;lbrack;Bakers&amp;rbrack;設定「儲存預處理場景檔案」已無法使用
* &amp;lbrack;平面投影&amp;rbrack;投影無法在有重複 UV 的網格上運作
* &amp;lbrack;Decal&amp;rbrack;使用不同填充層投影模式時，正常通道行為的差異
* &amp;lbrack;Smudge&amp;rbrack;&amp;lbrack;Clone&amp;rbrack;在面具繪畫時可能會出現遺物
* &amp;lbrack;Engine&amp;rbrack;特定圖層內容的崩潰
* &amp;lbrack;Engine&amp;rbrack;有時塗裝時會隨機當機
* &amp;lbrack;Anchor point&amp;rbrack;對空遮罩的參考總是回傳白色
* &amp;lbrack;Export&amp;rbrack;某些特定堆疊配置未考慮的層
* &amp;lbrack;Export mesh&amp;rbrack;無法匯出包含特殊字元的路徑
* &amp;lbrack;匯出 Mesh&amp;rbrack;從 Linux 或 MacOS 匯出時無法讀取 glTF 檔案
* &amp;lbrack;匯入 mesh&amp;rbrack;重新匯入 DAE、PLY 或 glTF 無法如預期運作

**已知問題：**

* &amp;lbrack;Scripting&amp;rbrack;&amp;lbrack;JavaScript&amp;rbrack; 無法編輯新的 Curvature Baker 設定
* &amp;lbrack;Bakers&amp;rbrack;在 Linux 上使用 GPU 光線追蹤時當機
* &amp;lbrack;Export&amp;rbrack;&amp;lbrack;USD&amp;rbrack; 不應匯出已停用的材質集
* &amp;lbrack;Crash&amp;rbrack;在材質層疊後更換遮罩

## 版本 5

### 5.3.3 (2019.3.3)

*（發布日期：2020* 年 2 月 6 日）摘要： **錯誤修正並升級至 Iray 2019.3**

**補充：**

* 升級至 Iray 2019.3
* &amp;lbrack;Log&amp;rbrack;標示 Ryzen CPU 的舊 BIOS 導致烘焙時當機
* &amp;lbrack;ABR&amp;rbrack; 從 ABR α 抽取至書架

**修正：**

* &amp;lbrack;Baker&amp;rbrack;若高多邊形網格沒有 UV，烘焙失敗
* &amp;lbrack;Linux&amp;rbrack;自訂滑鼠捷徑不會被儲存
* &amp;lbrack;Brush&amp;rbrack;輪廓隨著某些 alpha 形狀消失
* &amp;lbrack;Tablet&amp;rbrack;移動滑桿時偵測不良
* &amp;lbrack;Shortcuts&amp;rbrack;無法用「Ctrl+Alt+MouseClick」設定任何捷徑。
* &amp;lbrack;Shelf&amp;rbrack;使用繪圖板時無法看到資源提示
* &amp;lbrack;2D View&amp;rbrack;&amp;lbrack;Export&amp;rbrack; 2D View 預設不考慮一般資訊
* 用某些畫筆在 UV 對齊時會凍結
* 在濾鏡下作畫會在持續的筆觸上產生假象
* &amp;lbrack;Viewport&amp;rbrack;重新匯入網格後，viewport 材質快取錯誤
* &amp;lbrack;Crash&amp;rbrack;匯出到 Photoshop 後儲存時出現錯誤
* &amp;lbrack;Crash&amp;rbrack;在匯入資源時以前綴寫入特殊符號
* &amp;lbrack;Crash&amp;rbrack;點擊 Anchor Point Properties 中的參考資料
* &amp;lbrack;錨點&amp;rbrack;當錨點與參考之間有濾波器時，通道不會更新
* 說明選單中的 Iray 網址連結無法使用

**已知問題：**

* &amp;lbrack;UV 展開&amp;rbrack;處理高多邊形網格可能需要很長時間
* &amp;lbrack;UV 展開&amp;rbrack;完全相同座標的頂點會合併
* &amp;lbrack;UV 展開&amp;rbrack;在某些罕見情況下，UV 生成可能會在某些網格部分失敗
* &amp;lbrack;UV 展開&amp;rbrack;在某些情況下，單一 UV 島的像素比不均勻或高度失真
* &amp;lbrack;UV 展開&amp;rbrack;材質集間的非均勻像素比率
* &amp;lbrack;UV 展開&amp;rbrack;產生的 UV 島嶼有時會非常拉長，且在某些情況下無法放入 UV 空間
* &amp;lbrack;UV 展開&amp;rbrack;退化面或非三角形網格面且邊緣小或重疊，可能無法展開 UV

### 5.3.2 (2019.3.2)

*（發布日期：2020* 年 1 月 21 日）摘要： **錯誤修正**

**修正：**

* 開啟以單通道模式儲存的專案時，網格不會顯示
* 用複製工具在圖層下繪製時，視窗並不總是更新

**已知問題：**

* &amp;lbrack;Bakers&amp;rbrack;與 Ryzen CPU 多執行緒相關的當機
* &amp;lbrack;UV 展開&amp;rbrack;處理高多邊形網格可能需要很長時間
* &amp;lbrack;UV 展開&amp;rbrack;完全相同座標的頂點會合併
* &amp;lbrack;UV 展開&amp;rbrack;在某些罕見情況下，UV 生成可能會在某些網格部分失敗
* &amp;lbrack;UV 展開&amp;rbrack;在某些情況下，單一 UV 島的像素比不均勻或高度失真
* &amp;lbrack;UV 展開&amp;rbrack;材質集間的非均勻像素比率
* &amp;lbrack;UV 展開&amp;rbrack;產生的 UV 島嶼有時會非常拉長，且在某些情況下無法放入 UV 空間
* &amp;lbrack;UV 展開&amp;rbrack;退化面或非三角形網格面且邊緣小或重疊，可能無法展開 UV

### 5.3.1 (2019.3.1)

*（發布日期：2019*&#x200B;年12月20日）摘要： **熱修補**

**修正：**

* 在處理具有特定 UV 投影的網格時會當機
* &amp;lbrack;ABR&amp;rbrack;切換 Photoshop 預設時會當機
* &amp;lbrack;Linux&amp;rbrack;因 libGLX 依賴問題，無法在 CentOS 7.4 上啟動 Substance Painter
* &amp;lbrack;Bakers&amp;rbrack;使用檔案> Clean後烘焙時當機
* &amp;lbrack;Bakers&amp;rbrack; 烘焙進度對話框在取消後凍結
* &amp;lbrack;Bakers&amp;rbrack;匯出材質後烘焙網格無法運作
* &amp;lbrack;Bakers&amp;rbrack;使用「依姓名匹配」的黑色網格地圖結果
* &amp;lbrack;Bakers&amp;rbrack;籠子不被考慮
* &amp;lbrack;Shelf&amp;rbrack;匯入 PSD 檔案會導致圖片損壞
* &amp;lbrack;Sample&amp;rbrack;「Mat」樣本專案有壞掉的攝影機和錯誤的匯出預設

**已知問題：**

* &amp;lbrack;Bakers&amp;rbrack;與 Ryzen CPU 多執行緒相關的當機
* &amp;lbrack;UV 展開&amp;rbrack;處理高多邊形網格可能需要很長時間
* &amp;lbrack;UV 展開&amp;rbrack;完全相同座標的頂點會合併
* &amp;lbrack;UV 展開&amp;rbrack;在某些罕見情況下，UV 生成可能會在某些網格部分失敗
* &amp;lbrack;UV 展開&amp;rbrack;在某些情況下，單一 UV 島的像素比不均勻或高度失真
* &amp;lbrack;UV 展開&amp;rbrack;材質集間的非均勻像素比率
* &amp;lbrack;UV 展開&amp;rbrack;產生的 UV 島嶼有時會非常拉長，且在某些情況下無法放入 UV 空間
* &amp;lbrack;UV 展開&amp;rbrack;退化面或非三角形網格面且邊緣小或重疊，可能無法展開 UV

### 5.3.0 (2019.3.0)

*（發布日期：2019* 年 12 月 17 日）摘要： **重大更新，提升手繪用戶體驗、與平板相容、自動 UV 展開測試版（0.3.0）及多元新手繪內容**

**補充：**

* 在 Substance Painter 中整合自動 UV 展開 0.3.0 版本
* &amp;lbrack;UV 展開&amp;rbrack;在 Substance Painter 中，當沒有 UV 存在或部分 UV 時，自動展開 UV
* &amp;lbrack;UV 解包&amp;rbrack;一個全域設定可啟用與停用
* &amp;lbrack;UV 解包&amp;rbrack;版本報告於日誌檔
* &amp;lbrack;UV 展開&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 表示 UV 展開進度
* &amp;lbrack;UI&amp;rbrack;在情境工具列新增設定，可選擇筆刷預覽：完整預覽、筆刷輪廓與準星
* &amp;lbrack;Tool&amp;rbrack;alpha區新增進階混合模式：除一般外，還要變亮（最大）
* &amp;lbrack;Layer Stack&amp;rbrack;每層的 Gamma 校正選項用於 alpha 或遮罩（右鍵選單）
* &amp;lbrack;Layer Stack&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 當層 alpha 經過伽瑪校正時，新增 &#39;i&#39; 圖示
* &amp;lbrack;Tablet&amp;rbrack;&amp;lbrack;Tool&amp;rbrack; 暴露尺寸與流量的最小壓力
* &amp;lbrack;Tablet&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 在情境工具列新增設定，可選擇曲線壓力：線性、易入、易入出
* &amp;lbrack;Tablet&amp;rbrack;&amp;lbrack;UX&amp;rbrack; 新增 Ctrl+Alt+click 以捲動
* 匯入 Photoshop 筆刷預設（ABR 格式）
* &amp;lbrack;ABR&amp;rbrack;支撐形狀參數
* &amp;lbrack;ABR&amp;rbrack; 支援形狀動力學參數
* &amp;lbrack;ABR&amp;rbrack;支援傳輸參數
* &amp;lbrack;ABR&amp;rbrack; 支援散射參數
* &amp;lbrack;ABR&amp;rbrack;&amp;lbrack;動態筆劃&amp;rbrack;支撐圓潤與翻轉
* &amp;lbrack;ABR&amp;rbrack;&amp;lbrack;Shelf&amp;rbrack; 在篩選編輯器中揭露刷子資料夾結構
* &amp;lbrack;ABR&amp;rbrack;&amp;lbrack;Shelf&amp;rbrack; 在縮圖中加入 Photoshop 圖示
* &amp;lbrack;ABR&amp;rbrack;&amp;lbrack;Shelf&amp;rbrack; 在 ABR 詳細縮圖中新增不支援參數列表
* &amp;lbrack;Tool&amp;rbrack;&amp;lbrack;動態筆劃&amp;rbrack; 新的動態筆劃設定，用來控制產生多少隨機種子
* &amp;lbrack;Tool&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 新增散射抖動的分布與軸設定
* &amp;lbrack;Shortcut&amp;rbrack; 新增 Ctrl+Shift+B 以開啟烘焙視窗
* &amp;lbrack;UI&amp;rbrack;&amp;lbrack;Menu&amp;rbrack; 在「編輯」選單中新增條目以開啟烘焙視窗
* &amp;lbrack;UI&amp;rbrack;&amp;lbrack;Settings&amp;rbrack; 縮短指令列表的改進對齊
* &amp;lbrack;UI&amp;rbrack;將壓力控制（大小與流量）圖示替換為開關按鈕
* &amp;lbrack;視窗&amp;rbrack; 允許分別聚焦 2D 與 3D 視窗
* 更新至 QT 5.12.5
* &amp;lbrack;UI&amp;rbrack; 表示網格載入進度
* &amp;lbrack;Substance&amp;rbrack;新增非夾具及軟範圍滑桿支援
* &amp;lbrack;Substance&amp;rbrack;將Substance參數精度提升至6位小數點
* &amp;lbrack;Substance&amp;rbrack;考慮由參數定義的步驟
* &amp;lbrack;Substance&amp;rbrack;優化動態筆觸生成，支援使用者資料中的條件
* &amp;lbrack;Substance&amp;rbrack;允許透過使用者資料將圖形輸出指定為所有通道的遮罩
* &amp;lbrack;Content&amp;rbrack;更新「Mat」範例專案，加入位移友善拓撲、新的 ID 映射及新相機
* &amp;lbrack;內容&amp;rbrack; 整合三種新濾鏡（MatFx）：漫畫書、水彩、油畫（靈感來自Emrecan Cubukcu作品）
* &amp;lbrack;內容&amp;rbrack;整合 Kyle T. Webster 套件中的 102 個 Photoshop 筆刷預設
* &amp;lbrack;內容&amp;rbrack; 整合18個新的筆刷預設：Paint Roller Arrow、Paint Roller Warning文字、Charcoal Fine等
* &amp;lbrack;內容&amp;rbrack; 整合9個新alpha：Brush Maker Paint Roller、Brush Maker Photoshop、Brush Pattern 等
* &amp;lbrack;內容&amp;rbrack; 整合兩個新工具預設：Gouache Dense 與 Gouache Faded
* &amp;lbrack;Content&amp;rbrack; 整合 1 個新產生器：UV 檢查器（標示 UV 島嶼與接縫）
* &amp;lbrack;內容&amp;rbrack; 整合兩個新的匯出預設：Keyshot 9+ 和 Spark AR Studio
* &amp;lbrack;內容&amp;rbrack; 整合 1 個新專案範本：Spark AR Studio（Facebook）

**修正：**

* &amp;lbrack;Tablet&amp;rbrack;還原觸控筆筆劃（Ctrl+Z）比還要延遲
* &amp;lbrack;Tablet&amp;rbrack;畫直線時不考慮開始與結束壓力
* &amp;lbrack;Tablet&amp;rbrack;使用直線時，第一枚郵票會畫兩次
* &amp;lbrack;Tablet&amp;rbrack;改善對Huion平板捷徑的支援
* &amp;lbrack;Tablet&amp;rbrack;提升對Huion筆按鈕的支援
* &amp;lbrack;平板&amp;rbrack;筆刷預覽與繪製郵票之間的偏移
* &amp;lbrack;Tablet&amp;rbrack;用筆修改筆刷的捷徑在罕見情況下會導致效能下降
* &amp;lbrack;Tablet&amp;rbrack;在特定圖層上繪製時延遲
* 在切換視窗時，偶爾會出現模糊的貼圖
* &amp;lbrack;UI&amp;rbrack;&amp;lbrack;Substance&amp;rbrack; 影像輸入不一定會顯示
* Clean 不會移除專案中已匯入的預設
* &amp;lbrack;工具&amp;rbrack;&amp;lbrack;動態行程&amp;rbrack;調整印章週期數時的效能問題
* 在 3D/2D 視窗模式下繪製時，偶爾會出現刷新率問題
* 畫一筆很長的筆觸可能會導致凍結
* &amp;lbrack;工具&amp;rbrack;使用特定動態筆觸繪製時的效能問題
* &amp;lbrack;UI&amp;rbrack;上下文工具列在選擇資料夾時仍會顯示筆刷屬性
* 對稱軸值不會重置
* 匯入帶有浮點數值的 EXR 貼圖會完全黑
* Alt+點擊頻道來隔離，對濾波器和產生器都沒用
* &amp;lbrack;Export&amp;rbrack;特定專案在出口時崩潰
* &amp;lbrack;Substance&amp;rbrack;若參數被 Visible 隱藏，下拉選單預設值不正確
* &amp;lbrack;Shader&amp;rbrack;透過材質分層定義的通道在介面中排序方式不同
* &amp;lbrack;Shelf&amp;rbrack;預設元資料不會儲存在磁碟上

**已知問題：**

* &amp;lbrack;UV 展開&amp;rbrack;處理高多邊形網格可能需要很長時間
* &amp;lbrack;UV 展開&amp;rbrack;完全相同座標的頂點會合併
* &amp;lbrack;UV 展開&amp;rbrack;在某些罕見情況下，UV 生成可能會在某些網格部分失敗
* &amp;lbrack;UV 展開&amp;rbrack;在某些情況下，單一 UV 島的像素比不均勻或高度失真
* &amp;lbrack;UV 展開&amp;rbrack;材質集間的非均勻像素比率
* &amp;lbrack;UV 展開&amp;rbrack;產生的 UV 島嶼有時會非常拉長，且在某些情況下無法放入 UV 空間
* &amp;lbrack;UV 展開&amp;rbrack;退化面或非三角形網格面且邊緣小或重疊，可能無法展開 UV
* Meetmat 範例在進口攝影機時有一些問題

### 5.2.3 (2019.2.3)

*（發布日期：2019*&#x200B;年10月23日）摘要： **錯誤修正釋出**

**補充：**

* &amp;lbrack;貼圖集合列表&amp;rbrack; 新增按鈕以快速啟用或停用對焦模式
* &amp;lbrack;Log&amp;rbrack; 在日誌檔中新增 Windows 10 版本號
* 更新至最新版本的 Substance Engine。
* &amp;lbrack;MacOS&amp;rbrack;公證軟體以符合新的 MacOS Catalina 發行要求

**修正：**

* &amp;lbrack;Plugin&amp;rbrack;插件來源無法運作
* &amp;lbrack;MacOS&amp;rbrack;&amp;lbrack;Shader&amp;rbrack;Mac OS 10.14.5 與 AMD：材質分層無法如預期運作

**已知問題：**

* 帶有細分的 Alembic 檔案無法匯入
* 匯入某些 Alembic 檔案時罕見地當機
* 在 Pascal GPU 上用 DXR 烘焙時，UI 暫時沒有反應

### 5.2.2 (2019.2.2)

*（發布日期：2019* 年 9 月 20 日）摘要： **錯誤修正釋出**

**修正：**

* 透過腳本匯入資源可能導致當機
* &amp;lbrack;Plugin&amp;rbrack;從原始碼下載素材可能會導致當機

**已知問題：**

* 帶有細分的 Alembic 檔案無法匯入
* 匯入某些 Alembic 檔案時罕見地當機
* 在 Pascal GPU 上用 DXR 烘焙時，UI 暫時沒有反應

### 5.2.1 (2019.2.1)

*（發布日期：2019* 年 9 月 17 日）摘要： **錯誤修正釋出**

**修正：**

* &amp;lbrack;Mac&amp;rbrack;&amp;lbrack;USD&amp;rbrack;從 MacOS 匯出的 USDZ 檔案無法開啟
* &amp;lbrack;Texture Set&amp;rbrack;無法用 ALT 修改器分離材質集
* &amp;lbrack;Shelf&amp;rbrack;預設、智慧材料與智慧口罩在退出應用時都會被修改
* &amp;lbrack;Layer Stack&amp;rbrack;刪除其他效果後無法選擇效果
* 在工具屬性面板中使用滑桿時閃爍
* 匯出預設到架子時當機
* 匯出空間不足的預設時會當機
* 建立空間不足的預設時會當機

**已知問題：**

* 帶有細分的 Alembic 檔案無法匯入
* 匯入某些 Alembic 檔案時罕見地當機
* 在 Pascal GPU 上用 DXR 烘焙時，UI 暫時沒有反應

### 5.2.0 (2019.2.0)

*（發布日期：2019*&#x200B;年7月25日）摘要： **重大發行，包含烘焙師在性能上的更新，以及新增的預視覺化模式+新內容**

**補充：**

* &amp;lbrack;Bakers&amp;rbrack;新增對 GPU 光線追蹤的支援，支援 DXR 與 OptiX（環境光遮蔽、厚度）
* &amp;lbrack;Bakers&amp;rbrack;CPU 光線追蹤的優化與加速
* &amp;lbrack;Bakers&amp;rbrack;&amp;lbrack;Vis mode&amp;rbrack;&amp;lbrack;UI&amp;rbrack; View port in New baking visualization mode
* &amp;lbrack;Bakers&amp;rbrack;&amp;lbrack;Preferences&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 新烘焙選項用於啟用-停用GPU Raytracing
* &amp;lbrack;Bakers&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 進度條對話框的重製
* &amp;lbrack;Bakers&amp;rbrack;改進警告與錯誤訊息
* &amp;lbrack;Bakers&amp;rbrack;允許更靈敏的烘焙取消流程
* &amp;lbrack;Bakers&amp;rbrack;點擊取消後重新開啟烘焙視窗
* &amp;lbrack;Proj&amp;rbrack;&amp;lbrack;UX&amp;rbrack; 旋轉操作手的可用性改進
* &amp;lbrack;設定&amp;rbrack; 透過降低 HDPI 螢幕的視窗解析度來提升效能的選項
* &amp;lbrack;腳本&amp;rbrack; 變更材質集解析度
* &amp;lbrack;Scripting&amp;rbrack; 取得選取的貼圖集
* &amp;lbrack;腳本&amp;rbrack; 允許使用者選擇材質集
* &amp;lbrack;Scripting&amp;rbrack; 用來知道材質集選擇何時更改
* &amp;lbrack;Shelf&amp;rbrack;新增40種智慧材料
* &amp;lbrack;Shelf&amp;rbrack;新增20款智慧口罩

**修正：**

* &amp;lbrack;堆疊&amp;rbrack;多重選取圖層時 UI 凍結
* &amp;lbrack;堆疊;堆疊多層會讓介面凍結時間比平常更長
* &amp;lbrack;疊疊&amp;rbrack;在某些情況下，可以同時選取圖層與效果
* 繪畫工具中使用的物質圖並非以正確解析度產生
* &amp;lbrack;Baker&amp;rbrack;「烘焙所有材質集」按鈕在未選擇烘焙者時不會被停用
* &amp;lbrack;MacOS&amp;rbrack;停用關於拼貼的警告訊息
* 投影工具搭配遮罩使用時沒有預覽功能
* 當嘗試儲存且磁碟空間不足時，專案會當機和損壞
* &amp;lbrack;Shelf&amp;rbrack;當磁碟資源透過 shelf 匯入時空間不足
* &amp;lbrack;Shelf&amp;rbrack;恢復會話預設時會崩潰
* &amp;lbrack;Shelf&amp;rbrack;匯入以空格結尾的預設會導致當機
* &amp;lbrack;Shelf&amp;rbrack;將一個以空格結尾的前綴資源匯入會導致當機

**已知問題：**

* 帶有細分的 Alembic 檔案無法匯入
* 匯入某些 Alembic 檔案時罕見地當機
* 在 Pascal GPU 上用 DXR 烘焙時，UI 暫時沒有反應

### 5.1.3 (2019.1.3)

*（發布日期：2019* 年 7 月 1 日）摘要： **錯誤修正並新增兩項功能**

**補充：**

* 允許以命令列指定 VRam 預算（例如 --vram-budget 4096）
* &amp;lbrack;QML&amp;rbrack;揭露 wrapMode 及 QML 按鈕與勾選框的 elide 屬性

**修正：**

* 「跟隨路徑」並非每次都有效
* 頻道映射無法在單頻道插槽中使用的 SBSAR 上運作
* &amp;lbrack;圖層堆疊與rbrack;隱藏圖層捲動時效能低
* &amp;lbrack;TextureSet&amp;rbrack;點擊遮罩時當機
* &amp;lbrack;SVT&amp;rbrack;位移顯示不正確，有時會閃爍
* &amp;lbrack;Alembic&amp;rbrack;使用點法線取代頂點法線的網格崩潰
* &amp;lbrack;Alembic&amp;rbrack;&amp;lbrack;Log&amp;rbrack;若匯入時不支援 Alembic 檔案，請在日誌中回報錯誤

**已知問題：**

* 帶有細分的 Alembic 檔案無法匯入
* 匯入某些 Alembic 檔案時罕見地當機

### 5.1.2 (2019.1.2)

*（發布日期：2019*&#x200B;年5月21日）摘要： **熱修補**

**修正：**

* 在輸入影像時選擇兩個資源時會當機

### 5.1.1 (2019.1.1)

*（發布日期：2019*&#x200B;年5月20日）摘要： **熱修補**

**補充：**

* Substance Engine 最新版本，最新版本為 Substance Designer 2019.1

**修正：**

* &amp;lbrack;Substance&amp;rbrack;若未考慮輸入影像，則可見
* &amp;lbrack;SVT&amp;rbrack;&amp;lbrack;Engine&amp;rbrack; 改變材質集解析度在某些情況下會導致當機
* &amp;lbrack;Engine&amp;rbrack;在某些情況下會出現隨機的黑色材質
* &amp;lbrack;Layer Stack&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 使用 SHIFT 切換遮罩可同時選擇多個圖層
* &amp;lbrack;Layer Stack&amp;rbrack;不透明度對穿透混合模式下的繪圖效果沒有影響
* &amp;lbrack;Layer Stack&amp;rbrack; Height To Normal 濾鏡輸入無法隨著橡皮擦筆刷筆觸正確更新
* &amp;lbrack;LayersStack&amp;rbrack;當解除智慧遮罩的下落時會崩潰
* 線框閃爍陰影與時間抗鋸齒啟動
* &amp;lbrack;Displacement&amp;rbrack;在 AMD 上使用重度網格時會有延遲
* &amp;lbrack;Windows&amp;rbrack;透過檔案總管開啟某些專案時會當機
* &amp;lbrack;直方圖&amp;rbrack;在某些情況下移除帶有錨點的遮罩時會崩潰
* 在某些罕見情況下，預覽產生時會當機
* &amp;lbrack;Crash&amp;rbrack;無法用太多複製和模糊工具重新開啟專案
* 有些情況下，儲存後材質模式中沒有顯示網格
* &amp;lbrack;Scripting&amp;rbrack; alg.mapexport.documentStructure（） 會回傳錯誤的資料夾值

**已知問題：**

* 雙擊貼圖集名稱後，會在進入重新命名模式前選取它

### 5.1.0 (2019.1.0)

*（發行日期：2019* 年 4 月 23 日）摘要： **動態筆觸與專屬新內容、即時位移與鑲嵌、Iray 效果、比較遮罩效果、徑向對稱、平面投影與球面投影**

**補充：**

* &amp;lbrack;工具&amp;rbrack;動態筆觸：物質變化與筆觸同時進行
* &amp;lbrack;動態筆劃&amp;rbrack; 顯示帶有選項的新印章索引參數
* &amp;lbrack;動態劃法&amp;rbrack;考慮$time參數
* &amp;lbrack;動態筆劃&amp;rbrack;每筆劃及每枚印章產生新的$randomseed參數
* &amp;lbrack;動態筆劃&amp;rbrack;從隨機數字開始動態筆劃索引
* &amp;lbrack;動態筆劃&amp;rbrack;&amp;lbrack;Shelf&amp;rbrack; 協助尋找帶有專用新圖示的動態筆劃資源
* 即時視窗中的位移與鑲嵌
* Iray 中的位移與鑲嵌
* &amp;lbrack;Shader settings&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 新分頁用於控制位移與鑲嵌
* &amp;lbrack;Layer stack&amp;rbrack; 新 CompareMask 效果：透過比較兩個通道產生遮罩
* &amp;lbrack;Layer stack&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 右鍵選單新增「Add mask with height combination」以插入 CompareMask 效果
* &amp;lbrack;對稱&amp;rbrack;新對稱模式：放射狀繪畫
* &amp;lbrack;對稱設定&amp;rbrack;展開「設定」和「顯示」兩個區塊
* &amp;lbrack;對稱設定&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 放射狀繪畫預覽
* 顯示兩種新的投影模式：平面投影與球面投影
* &amp;lbrack;Proj&amp;rbrack;所有投影的新形狀裁切模式
* &amp;lbrack;Proj&amp;rbrack;平面模式搭配新操作手：Surface tool
* &amp;lbrack;Proj&amp;rbrack;&amp;lbrack;Shortcut&amp;rbrack; Surface 工具的快捷鍵 SHIFT+W
* &amp;lbrack;Proj&amp;rbrack;平面投影遮罩，含深度剔除與背面剔除
* &amp;lbrack;三軸旋轉操縱器在三軸上改進，用於三平面
* &amp;lbrack;Tool&amp;rbrack;&amp;lbrack;UX&amp;rbrack; Alt 點擊通道，聚焦該通道（啟用或停用其他通道）
* &amp;lbrack;引擎&amp;rbrack;更新至最新版本的Substance Engine。
* &amp;lbrack;貼圖集合&amp;rbrack;多重選取與變更解析度
* &amp;lbrack;Texture set&amp;rbrack;快速啟動與停用材質集
* &amp;lbrack;材質集合&amp;rbrack;將單人及所有選項合併到新選單中
* &amp;lbrack;Texture set&amp;rbrack;&amp;lbrack;Layer stack&amp;rbrack;新啟用與停用圖示
* &amp;lbrack;疊加 stack&amp;rbrack;&amp;lbrack;UX&amp;rbrack; 在已選取效果上方插入
* &amp;lbrack;Layer stack&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 重做層疊檢視選擇風格
* &amp;lbrack;Layer Stack&amp;rbrack;實例圖層的混合模式現在預設為 Pass Through 模式
* &amp;lbrack;Export&amp;rbrack;啟動與停用抖動的選項
* &amp;lbrack;Plugin&amp;rbrack; 支援滑桿的精確修飾鍵（SHIFT）
* &amp;lbrack;Plugin&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 自動儲存新圖示
* &amp;lbrack;Scripting&amp;rbrack; 列出資料夾內容
* &amp;lbrack;腳本&amp;rbrack; 允許刪除檔案
* &amp;lbrack;Scripting&amp;rbrack; 閱讀所有堆疊資訊，包括已使用資源
* &amp;lbrack;內容&amp;rbrack;&amp;lbrack;動態筆劃&amp;rbrack;新工具與筆刷預設
* &amp;lbrack;Content&amp;rbrack;&amp;lbrack;動態筆劃&amp;rbrack;兩個新的程序式漸層：漸層色調與漸層建構器
* &amp;lbrack;內容&amp;rbrack;11款新濾鏡：MatFx 剝落塗料、MatFx 水滴等
* &amp;lbrack;內容&amp;rbrack;7個新產生器：自動縫合器、UV 隨機色彩、UV 紋素密度等
* &amp;lbrack;內容&amp;rbrack; 93個新字母：新文字、箭頭及各種其他形狀
* &amp;lbrack;內容&amp;rbrack;兩個新程序化作品：漸層色調、漸層建構器等
* &amp;lbrack;內容&amp;rbrack;21 個動態筆觸工具與畫筆預設：Pebbles、Footprints、Spray 等
* &amp;lbrack;內容&amp;rbrack;2 新HDRis：Canopus Ground與Autumn Forest
* &amp;lbrack;內容&amp;rbrack;更新內容，並隨機整理種子於架上
* &amp;lbrack;內容&amp;rbrack;新圖示，書架中暴露隨機種子參數

**修正：**

* &amp;lbrack;Layers stack&amp;rbrack; Layer stack 一直拖拉下去
* &amp;lbrack;Mac&amp;rbrack;「搜尋顯示」可能導致凍結
* &amp;lbrack;Scripting&amp;rbrack; 若著色器檔案被移動，透過自訂介面儲存的設定會遺失
* &amp;lbrack;Scripting&amp;rbrack;API 版本號錯誤且不更新
* &amp;lbrack;Effect&amp;rbrack;直方圖內容未正確顯示
* &amp;lbrack;Effect&amp;rbrack;直方圖效果在某些情況下不會更新
* &amp;lbrack;Shelf&amp;rbrack;針腳未正確對齊於「塑膠布料金字塔」材質上。

**已知問題：**

* 雙擊貼圖集名稱後，會在進入重新命名模式前選取它
* &amp;lbrack;Layer Stack&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 使用 SHIFT 切換遮罩可同時選擇多個圖層

## 版本 4

### 4.3.3 (2018.3.3)

*（發布日期：2019* 年 3 月 7 日）摘要： **錯誤修正**

**補充：**

* &amp;lbrack;Content&amp;rbrack; 整合新專案範本：「PBR - 金屬粗糙度 Alpha 混合」
* Linux 動態函式庫搜尋順序改為優先將安裝目錄中的函式庫置於系統已安裝的函式庫之前

**修正：**

* 網格有時會從 3D 視窗消失（按 F 重置相機）
* 更新 Substance Painter Sketchfab 上傳器，使用新的 Sketchfab 授權類型
* &amp;lbrack;Import&amp;rbrack;&amp;lbrack;glTF&amp;rbrack; 錯誤處理 glTF 檔案中定義的輸入材質調變
* &amp;lbrack;Import&amp;rbrack;&amp;lbrack;glTF&amp;rbrack; glTF 匯入時地面平面有時會錯誤顯示
* &amp;lbrack;出口&amp;rbrack;&amp;lbrack;USD&amp;rbrack;不透明度在Arkit中無法運作
* &amp;lbrack;出口&amp;rbrack;&amp;lbrack;USD&amp;rbrack;USDz 出口在某些情況下崩盤
* &amp;lbrack;出口&amp;rbrack;&amp;lbrack;USD&amp;rbrack;出口至美元卻不節省成本，導致崩盤
* &amp;lbrack;Export&amp;rbrack;&amp;lbrack;USD&amp;rbrack; 貼圖平鋪模式錯誤，網格分割模式錯誤，著色器輸出類型錯誤
* &amp;lbrack;Export&amp;rbrack;&amp;lbrack;USD&amp;rbrack; 僅部分材質集的稀疏匯出，包含所有幾何體
* &amp;lbrack;Instance&amp;rbrack;嘗試刪除破損實例層時會當機
* &amp;lbrack;回歸&amp;rbrack;&amp;lbrack;Export&amp;rbrack; 部分未匯出至指定位元深度的映射
* &amp;lbrack;Linux&amp;rbrack;函式庫 libtbb.so.2 的問題

**已知問題：**

* 在某些情況下，AMD VEGA GPU 會出現計算凍結的情況
* Huion 平板在 Windows 作業系統上出現捷徑的問題

### 4.3.2 (2018.3.2)

*（發布日期：2019* 年 1 月 24 日）摘要： **帶新功能的熱修補（USDZ 匯出與視口材質過濾）**

**補充：**

* &amp;lbrack;出口&amp;rbrack;允許出口至USDZ
* &amp;lbrack;Viewport&amp;rbrack;允許在顯示設定中控制材質品質
* &amp;lbrack;Viewport&amp;rbrack;在顯示設定中新增 mip 偏壓設定
* &amp;lbrack;Viewport&amp;rbrack;在顯示設定中加入各向異性濾波
* &amp;lbrack;plugins&amp;rbrack;更新官方插件以使用 Substance Painter 2018 的風格
* &amp;lbrack;License&amp;rbrack;預設安裝授權於使用者資料夾

**修正：**

* 墜機與減壓有關
* 在獨奏曲目上加入TAA（TAA）
* 搭配陰影的雜訊、TAA 和帶有抖動的 alpha 測試著色器
* 移除所有經典 PBR 著色器的鏡面抖動
* 在某些情況下，著色器設定會當機
* OpenGL 與 Iray 渲染之間的散射啟動並未同步
* 模糊和複製工具在特定網格上已經無法使用了
* 有些貼圖集無法出現在 Iray 渲染中
* 關閉專案後，已命名的材質集不會被儲存
* 在 ID 貼圖上拖放材質時，線框產生的瑕疵
* &amp;lbrack;Scripting&amp;rbrack; 儲存專案時不會強制建立檔案路徑
* &amp;lbrack;Scripting&amp;rbrack; 回調「onProjectAboutToSave（）」不再有效
* 論壇連結在回報錯誤視窗中斷裂

**已知問題：**

* 在某些情況下，AMD VEGA GPU 會出現計算凍結的情況
* Huion 平板在 Windows 作業系統上出現捷徑的問題

### 4.3.1 (2018.3.1)

*（發布日期：2018*&#x200B;年12月6日）摘要： **熱修補**

**補充：**

* &amp;lbrack;對稱性&amp;rbrack;&amp;lbrack;Viewport&amp;rbrack; 2D 視圖的對稱繪製回歸，且現在修正了複製筆刷預覽功能

**修正：**

* &amp;lbrack;Export&amp;rbrack;2D 視圖匯出時，有時會輸出黑色貼圖
* &amp;lbrack;Iray&amp;rbrack;在實例化材質層後，Iray 的正常資訊會變得不正確
* 非方形的貼圖集有時會導致當機
* &amp;lbrack;復原&amp;rbrack;幾個 Ctrl+Z 有時會隨機導致當機
* &amp;lbrack;QML&amp;rbrack;AlgScrollView 在某些情況下可以在日誌中建立警告（綁定迴圈）

**已知問題：**

* 在某些情況下，AMD VEGA GPU 會出現計算凍結的情況
* Huion 平板在 Windows 作業系統上出現捷徑的問題
* 抗鋸齒與陰影同時啟用時，可能會產生意想不到的效果

### 4.3.0 (2018.3.0)

*（發行日期：2018* 年 11 月 20 日）摘要： **視窗升級、正確的 2D 視圖匯出、新的 UI 輔助工具、強化的對稱工具、新內容以及大幅提升的效能**

**補充：**

* &amp;lbrack;抗鋸齒&amp;rbrack;&amp;lbrack;Viewport&amp;rbrack;新的 3D 視窗抗鋸齒過濾（透過顯示設定）
* &amp;lbrack;Export&amp;rbrack; 將 2D 視窗的內容匯出為單一材質
* &amp;lbrack;Export&amp;rbrack;&amp;lbrack;Dithering&amp;rbrack; 在 export 時暴露抖動
* &amp;lbrack;圖層疊加與資料夾上的顏色
* &amp;lbrack;層疊疊&amp;rbrack;快速啟動與停用多層及效果
* &amp;lbrack;疊加 stack&amp;rbrack;使用上下鍵和滑鼠捲動，更方便混合模式
* &amp;lbrack;Proj&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 三軸的額外旋轉操作器，適用於三平面
* &amp;lbrack;Proj&amp;rbrack;&amp;lbrack;Shorcuts&amp;rbrack; - 和 + 以改變 UV 投影操控器的大小
* &amp;lbrack;Shader&amp;rbrack;在 PBR 塗層著色器中控制塗層參數，並使用通道
* &amp;lbrack;Substance&amp;rbrack;為濾鏡與產生器暴露新的網格材質輸入
* &amp;lbrack;Symmetry&amp;rbrack;&amp;lbrack;Viewport&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 控制對稱偏移與操作員
* &amp;lbrack;Symmetry&amp;rbrack;&amp;lbrack;Contextual toolbar&amp;rbrack;&amp;lbrack;UI&amp;rbrack; 新對稱面板及選項
* &amp;lbrack;對稱性&amp;rbrack;新的對稱線交集模式
* &amp;lbrack;對稱性&amp;rbrack;新的對稱克隆游標
* &amp;lbrack;對稱性&amp;rbrack;&amp;lbrack;Shortcuts&amp;rbrack; Q 可隱藏，-， + 可改變大小，Shift 可切換為吸附
* &amp;lbrack;Log&amp;rbrack;無法匯出貼圖時改善錯誤訊息
* &amp;lbrack;腳本&amp;rbrack;允許在顯示設定中更改或更新資源
* &amp;lbrack;腳本&amp;rbrack; 允許在紋理集中建立或移除通道
* &amp;lbrack;Content&amp;rbrack;&amp;lbrack;Shaders&amp;rbrack; 新增對各向異性（pbr-metal-rough-anisopy-angle）著色器的支援
* &amp;lbrack;內容&amp;rbrack;預覽球體的更新，包含各向異性與修改角度
* &amp;lbrack;內容&amp;rbrack;更新 matFx 關閉線
* &amp;lbrack;內容&amp;rbrack;全新 Texturing.XYZ 無縫臉部掃描
* &amp;lbrack;內容&amp;rbrack;新異性程序劇
* &amp;lbrack;內容&amp;rbrack;新濾鏡：烘焙光照環境
* &amp;lbrack;內容&amp;rbrack;新環境地圖：studio automotive neutral
* &amp;lbrack;Content&amp;rbrack;新專案範本：PBR - 金屬粗糙度各向異性角度（含各向異性通道）
* &amp;lbrack;內容&amp;rbrack;新專案範本：PBR - 金屬粗糙度塗層
* &amp;lbrack;SVT&amp;rbrack;&amp;lbrack;Engine&amp;rbrack; Sparse Virtual Textures （SVT）
* &amp;lbrack;SVT&amp;rbrack;&amp;lbrack;Preferences&amp;rbrack;&amp;lbrack;UI&amp;rbrack; SVT 硬體支援加速選項
* &amp;lbrack;SVT&amp;rbrack;&amp;lbrack;Log&amp;rbrack;稀疏虛擬貼圖功能（例如磁碟大小）的額外資訊
* &amp;lbrack;SVT&amp;rbrack;&amp;lbrack;UI&amp;rbrack;如果磁碟容量過低，則在快取空間中顯示訊息視窗
* &amp;lbrack;SVT&amp;rbrack;&amp;lbrack;Preferences&amp;rbrack;&amp;lbrack;UI&amp;rbrack; Substance Painter 全域快取位置
* &amp;lbrack;SVT&amp;rbrack;新增環境變數以指定 Substance Painter 快取路徑
* &amp;lbrack;SVT&amp;rbrack;新的環境變數以啟動 SVT 硬體加速支援
* &amp;lbrack;SVT&amp;rbrack;偵測硬體的稀疏支援
* &amp;lbrack;SVT&amp;rbrack;&amp;lbrack;硬體稀疏&amp;rbrack;提高 Nvidia GPU 的最低驅動程式版本
* &amp;lbrack;SVT&amp;rbrack;&amp;lbrack;Shader&amp;rbrack;&amp;lbrack;Viewport&amp;rbrack;&amp;lbrack;UI&amp;rbrack;若存在 Sparse Virtual Texturing 的雜訊，則在專案開啟時警告使用者

**修正：**

* &amp;lbrack;Color Picker&amp;rbrack;嘗試選擇顏色時出現的繪製游標
* 透過選擇或取消選取特定順序的圖層而導致當機
* 貼上一個帶有遮罩的圖層實例時會當機
* &amp;lbrack;User Channel&amp;rbrack;&amp;lbrack;Regression&amp;rbrack;用戶頻道重命名時崩潰
* &amp;lbrack;使用者頻道&amp;rbrack;灰色刷子預覽
* &amp;lbrack;Alembic&amp;rbrack;進口後僅有一個材質材質的貼圖集
* &amp;lbrack;Engine&amp;rbrack;匯出的材質與刷子印記的視窗不同
* &amp;lbrack;Engine&amp;rbrack;帶有關卡效果的反推不會完全影響貼圖
* 材料選擇器是在撥打時用刷子劃過
* 把解析度切換到 128x128px 會導致當機
* 網格地圖連結在重新烘焙或實例化圖層時沒有正確更新
* &amp;lbrack;Substance&amp;rbrack; UserData ColorSpace 無法在 Baked Mesh Normal 輸入中運作
* 使用多個著色器實例時的 MDL 關聯不匹配
* &amp;lbrack;對稱性&amp;rbrack;&amp;lbrack;填充層&amp;rbrack;對稱平面及其操作器在填充層中啟動
* &amp;lbrack;Viewport&amp;rbrack;點擊後翻譯的樞軸點不一定更新
* &amp;lbrack;UI&amp;rbrack;修正圖示並移除 HDPI 顯示器的佔位符

**已知問題：**

* 在某些情況下，AMD VEGA GPU 會出現計算凍結的情況
* Huion 平板在 Windows 作業系統上出現捷徑的問題
* 抗鋸齒與陰影同時啟用時，可能會產生意想不到的效果

### 4.2.3 (2018.2.3)

*（發行日期：2018年9月25日）*

**修正：**

* &amp;lbrack;2D View&amp;rbrack;2D View 在建立新專案時會破壞某些網格
* &amp;lbrack;Crash&amp;rbrack;從 UV 投影切換到三平面投影會導致崩潰
* &amp;lbrack;RayCollider&amp;rbrack;因「RayCollider」多次當機
* &amp;lbrack;Tool&amp;rbrack;切換圖層會失去修改過的刷子屬性
* 切換到橡皮擦時，筆刷設定會被重置

**已知問題：**

* AMD VEGA GPU 的計算凍結問題
* Huion 平板在 Windows 作業系統上出現捷徑的問題

### 4.2.2 (2018.2.2)

*（發布日期：2018* 年 9 月 11 日）摘要： **熱修補內容更新、新增腳本功能，並可關閉自動更新功能**

**補充：**

* &amp;lbrack;內容&amp;rbrack;&amp;lbrack;Shelf&amp;rbrack; 新增皮膚架子預設
* &amp;lbrack;內容&amp;rbrack;&amp;lbrack;shelf&amp;rbrack; 將19個皮膚法線轉換為用於次表面散射的材料
* &amp;lbrack;Scripting&amp;rbrack;從開啟專案建立專案範本
* &amp;lbrack;Scripting&amp;rbrack; 取得/設定已開啟專案的匯出設定
* &amp;lbrack;Updates&amp;rbrack;能夠從設定和環境變數中關閉自動更新彈窗
* &amp;lbrack;更新&amp;rbrack;在維護過時的彈出視窗中顯示「未等到下一個版本」

**修正：**

* &amp;lbrack;攝影機&amp;rbrack;從正交切換到透視時變焦錯誤
* &amp;lbrack;Display&amp;rbrack;有些地圖以線性方式顯示，而非 sRGB
* &amp;lbrack;viewports&amp;rbrack;網格焦點表現不正常
* &amp;lbrack;2D View&amp;rbrack;壞掉的相機專案有消失的 UV Shells
* &amp;lbrack;SSS&amp;rbrack;&amp;lbrack;Tooltip&amp;rbrack; 地下散射工具提示會出現在日誌中
* 有些專案無法在 2018.2 中開啟，且錯誤訊息無法儲存 null substance 套件
* &amp;lbrack;Mask&amp;rbrack;在使用遮罩時，繪圖工具的顏色在某些情況下可能會卡住
* &amp;lbrack;Material&amp;rbrack;地圖在特定情況下未出現
* &amp;lbrack;Proj&amp;rbrack;&amp;lbrack;Tools&amp;rbrack; 操作手帶產生器啟動
* &amp;lbrack;Substance&amp;rbrack;缺少的Substance參數群組
* &amp;lbrack;腳本&amp;rbrack;文件中軟體名稱錯誤
* &amp;lbrack;UDIMs&amp;rbrack;日誌中沒有關於多個 UV 圖塊上 UV 殼層的資訊

**已知問題：**

* AMD VEGA GPU 的計算凍結問題
* Huion 平板在 Windows 作業系統上出現捷徑的問題

### 4.2.1 (2018.2.1)

*（發行日期：2018年8月3日）*

**修正：**

* 升級專案時缺少的次表面散射著色器參數

**已知問題：**

* AMD VEGA GPU 的計算凍結問題
* Huion 平板在 Windows 作業系統上出現捷徑的問題

### 4.2.0 (2018.2.0)

*（發布日期：2018* 年 8 月 2 日）摘要： **夏季發行、地下散射支援、投影與填充改進、相機匯入與選取、Alembic 與 glTF 支援、ID 地圖拖放功能、改良的 Substance 格式支援及新內容**

**補充：**

* &amp;lbrack;SSS&amp;rbrack;&amp;lbrack;Viewport&amp;rbrack;&amp;lbrack;Iray&amp;rbrack; Generic subsurface scattering
* &amp;lbrack;SSS&amp;rbrack;同步 MDL 與地下散射參數
* &amp;lbrack;SSS&amp;rbrack;新增一個名為 Scattering 的灰階通道
* &amp;lbrack;SSS&amp;rbrack;&amp;lbrack;著色器設定&amp;rbrack; 次表面散射（皮膚或半透明）的散射類型參數
* &amp;lbrack;SSS&amp;rbrack;&amp;lbrack;Shader Settings&amp;rbrack; 次表面散射的散射尺度參數
* &amp;lbrack;SSS&amp;rbrack;&amp;lbrack;Shader Settings&amp;rbrack; 次表面散射的色彩參數
* &amp;lbrack;SSS&amp;rbrack;&amp;lbrack;顯示設定&amp;rbrack;次表面散射的散射樣本計數
* &amp;lbrack;Shader&amp;rbrack;&amp;lbrack;Iray&amp;rbrack; 為 Iray 整合地下散射 MDL
* &amp;lbrack;Shader&amp;rbrack; 透過資源更新器更新著色器更新
* &amp;lbrack;Shader&amp;rbrack;更新變更日誌 API 與文件
* &amp;lbrack;工具屬性&amp;rbrack;&amp;lbrack;Proj&amp;rbrack; 三平面投影的新參數
* &amp;lbrack;Viewport&amp;rbrack;&amp;lbrack;Proj&amp;rbrack;直接用操作手控制 3D 視圖填充層屬性（三平面投影）
* &amp;lbrack;捷徑&amp;rbrack;&amp;lbrack;Proj&amp;rbrack;新捷徑Q、W、E、R、T用於三平面投影操作器
* &amp;lbrack;Viewport&amp;rbrack;&amp;lbrack;Proj&amp;rbrack;直接用操作器控制2D視圖中的填充層屬性（UV投影）
* &amp;lbrack;捷徑&amp;rbrack;&amp;lbrack;Proj&amp;rbrack; 新的 UV 投影操作手捷徑 Q
* &amp;lbrack;Contextual Toolbar&amp;rbrack;&amp;lbrack;Proj&amp;rbrack; Control triplanar projection manipulators
* &amp;lbrack;Contextual Toolbar&amp;rbrack;&amp;lbrack;Proj&amp;rbrack; Control UV projection manipulators
* &amp;lbrack;工具屬性&amp;rbrack;用投影和模板工具停用貼圖平鋪
* &amp;lbrack;模板&amp;rbrack;使用投影工具/模板使用非方形影像
* &amp;lbrack;模板&amp;rbrack;允許在屬性視窗中控制平鋪模式
* &amp;lbrack;模板&amp;rbrack;Zoom 不會置中於非平鋪模板上
* &amp;lbrack;Cameras&amp;rbrack;從 Maya、Max、Blender、Modo、DAE 匯入攝影機
* &amp;lbrack;Cameras&amp;rbrack;&amp;lbrack;Viewport&amp;rbrack; 在視窗中選擇並控制匯入的攝影機
* &amp;lbrack;攝影機&amp;rbrack;&amp;lbrack;Iray&amp;rbrack; 在 Iray 中選擇並控制匯入攝影機
* &amp;lbrack;Cameras&amp;rbrack;&amp;lbrack;UI&amp;rbrack;&amp;lbrack;New project&amp;rbrack;&amp;lbrack;Project configuration&amp;rbrack; Import cameras 預設已勾選
* &amp;lbrack;攝影機&amp;rbrack;&amp;lbrack;Shortcuts&amp;rbrack; 新增快捷鍵以切換攝影機
* &amp;lbrack;Cameras&amp;rbrack;&amp;lbrack;Viewport&amp;rbrack; 在視窗中加入畫面
* &amp;lbrack;Cameras&amp;rbrack;&amp;lbrack;Viewport Settings&amp;rbrack; 控制影格不透明度
* &amp;lbrack;相機&amp;rbrack;&amp;lbrack;相機設定&amp;rbrack;最大焦距為500mm
* &amp;lbrack;攝影機&amp;rbrack;&amp;lbrack;攝影機設定&amp;rbrack; 曝光比例
* &amp;lbrack;Cameras&amp;rbrack;&amp;lbrack;相機設定&amp;rbrack; 新增鎖定選項
* &amp;lbrack;Cameras&amp;rbrack;&amp;lbrack;相機設定&amp;rbrack; 新增還原選項
* &amp;lbrack;Cameras&amp;rbrack;&amp;lbrack;相機設定&amp;rbrack; 新增對焦距離屬性
* &amp;lbrack;glTF&amp;rbrack; 匯入 glTF 檔案
* &amp;lbrack;glTF&amp;rbrack; 匯入環境遮蔽地圖
* &amp;lbrack;Alembic&amp;rbrack;匯入帶有靜態幾何的 Alembic 1 幀
* &amp;lbrack;Shelf&amp;rbrack;用 ID 映射搭配修飾鍵（CTRL/Command）直接拖放材質到網格上
* &amp;lbrack;Layer Stack&amp;rbrack;透過拖放材料在帶有 ID 映射的網格上自動建立 ID 遮罩
* &amp;lbrack;圖層堆疊&amp;rbrack;透過拖放自動捲動圖層堆疊
* &amp;lbrack;UI&amp;rbrack;&amp;lbrack;Tool Properties&amp;rbrack; Expose Substance 的預設
* &amp;lbrack;UI&amp;rbrack;&amp;lbrack;幫助選單&amp;rbrack; 說明選單的改進
* &amp;lbrack;UI&amp;rbrack;&amp;lbrack;新專案&amp;rbrack;&amp;lbrack;專案配置&amp;rbrack;視窗重組
* &amp;lbrack;UI&amp;rbrack;&amp;lbrack;新專案&amp;rbrack;&amp;lbrack;Project Configuration&amp;rbrack; 以檔案替換網格術語
* &amp;lbrack;UI&amp;rbrack;&amp;lbrack;Substance&amp;rbrack; UI 中顯示 Substance 屬性
* &amp;lbrack;快捷鍵&amp;rbrack;F4 可在 2D 與 3D 視圖間切換
* &amp;lbrack;捷徑&amp;rbrack;切換模板 N 與快速遮罩 U 的新捷徑
* &amp;lbrack;Substance 整合&amp;rbrack;考慮 Substance 參數中的「可見 if」陳述
* &amp;lbrack;Viewport&amp;rbrack;鏡頭移動後陰影不強制計算
* &amp;lbrack;內容&amp;rbrack;更新 MeetMat 並導入攝影機
* &amp;lbrack;Content&amp;rbrack; 新增啟用次表面散射的樣本 - JadeToad
* &amp;lbrack;Content&amp;rbrack; 新增一個啟用次表面散射的 PBR 專案範本
* &amp;lbrack;Content&amp;rbrack;更新匯出預設以新增散射通道
* &amp;lbrack;內容&amp;rbrack;&amp;lbrack;Shelf&amp;rbrack;新增以下次表面散射支援：pbr-metal-rough、pbr-metal-rough-alpha-test、pbr-塗層、pbr-spec-gloss。
* &amp;lbrack;內容&amp;rbrack;&amp;lbrack;Shelf&amp;rbrack;為5種智慧材料（彈珠與皮膚）新增散射通道
* &amp;lbrack;內容&amp;rbrack;&amp;lbrack;Shelf&amp;rbrack; 1 塊新玉材
* &amp;lbrack;內容&amp;rbrack;&amp;lbrack;Shelf&amp;rbrack;1 件新蠟材質

**修正：**

* &amp;lbrack;CMD&amp;rbrack;同一命令列不同版本的結果不同
* &amp;lbrack;TDR&amp;rbrack;如果 TdrLevel 有設定，你的日誌裡不會有任何錯誤
* &amp;lbrack;Baker&amp;rbrack;環境遮蔽地圖被翻轉
* &amp;lbrack;ID Map&amp;rbrack;在 0-1 範圍外挑選時會崩潰
* &amp;lbrack;Iray&amp;rbrack;切換材質集並回到繪圖模式時會當機
* &amp;lbrack;Viewport&amp;rbrack; 同步視窗間的下拉區域以便拖放
* &amp;lbrack;引擎&amp;rbrack;在鋪平鋪填充層或繪製小刷子時出現的莫爾痕跡
* &amp;lbrack;License&amp;rbrack;授權服務不良軟體版本檢查
* &amp;lbrack;License&amp;rbrack;重新設計我們處理認證的方式
* &amp;lbrack;API&amp;rbrack;即使在使用範本建立時，也呼叫 onNewProjectCreated 腳本 API 事件
* &amp;lbrack;Shader&amp;rbrack;編譯後的著色器不會從快取載入，當著色器檔案未編譯時
* &amp;lbrack;Shelf&amp;rbrack;從 Shelf 匯出 HDR 檔案會輸出一個帶有壓縮值的檔案
* &amp;lbrack;Export&amp;rbrack;EXR 匯出將 RGB 色彩值夾在 0-1 之間
* &amp;lbrack;內容&amp;rbrack;程序噪音 3D Perlin 噪音分形被像素化

**已知問題：**

* AMD VEGA GPU 的計算凍結問題
* Huion 平板在 Windows 作業系統上出現捷徑的問題

### 4.1.3 (2018.1.3)

*（發行日期：2018年6月28日）*

**補充：**

* &amp;lbrack;偏好設定&amp;rbrack;建議在 Painter 重新啟動時儲存專案

**修正：**

* &amp;lbrack;插件&amp;rbrack;搜尋物質來源無法運作
* &amp;lbrack;智慧材料的進口在某些情況下會導致崩盤
* &amp;lbrack;Smart Materials&amp;rbrack;刪除智慧材料在某些情況下會導致當機
* &amp;lbrack;儲存&amp;rbrack;存檔在某些罕見情況下會導致當機
* &amp;lbrack;Shelf&amp;rbrack;反推不適用於格子 2 和 格子 3
* &amp;lbrack;Shelf&amp;rbrack;某些 Alpha 字體有打字錯誤
* &amp;lbrack;Shelf&amp;rbrack;有些物質材質無法正確呈現

**已知問題：**

* AMD VEGA GPU 的計算凍結問題

### 4.1.2 (2018.1.2)

*（發行日期：2018*&#x200B;年6月12日）摘要： **改良烘焙速度、改良存檔系統、更新滑桿、更新外掛API、中文翻譯、新增可選的擴充功能**

**補充：**

* &amp;lbrack;Bakers&amp;rbrack;新烘焙版本的性能提升
* 與不相容的 GPU 強制顯示對話框
* &amp;lbrack;Save&amp;rbrack; 公開新的緊湊專案功能（完整/壓縮儲存模式）
* &amp;lbrack;Save&amp;rbrack;若存檔錯誤，請通知使用者
* &amp;lbrack;Clean&amp;rbrack;下一個存檔以完整/壓縮模式
* &amp;lbrack;滑桿&amp;rbrack;提升色彩/灰階條與滑桿的精度
* &amp;lbrack;滑桿&amp;rbrack;新增上下箭頭控制
* &amp;lbrack;滑桿&amp;rbrack;色彩與灰階條滑桿的偵測區域相同
* &amp;lbrack;Plugin&amp;rbrack; 自動儲存永遠以增量模式
* &amp;lbrack;Plugin&amp;rbrack; 切換插件為新介面風格的選項
* &amp;lbrack;語言&amp;rbrack;新增中文翻譯
* &amp;lbrack;Padding&amp;rbrack;在貼圖集設定中，依照貼圖集切換 UV 與 3D 空間鄰居填充的選項
* &amp;lbrack;Script&amp;rbrack; 顯示儲存模式：完整/壓縮或增量
* &amp;lbrack;Script&amp;rbrack; 更新腳本/QML 文件
* &amp;lbrack;Log&amp;rbrack;表示日誌中的儲存模式（完整/壓縮或增量）

**修正：**

* &amp;lbrack;Tool&amp;rbrack;通道槽在單通道填充時會轉變為材料槽
* 載入一個網格（FBX）時，有些面沒有被材質指派時會當機
* 在虛擬機上使用 NVIDIA GRID 5.2 在 Iray 中當機
* 當還原材質預設刪除時會崩潰
* 載入某些專案時會當機
* &amp;lbrack;命令列&amp;rbrack;UDIM新命令列，網格分割至UDIM
* &amp;lbrack;工具列&amp;rbrack; 工具列縮小
* &amp;lbrack;Instancing&amp;rbrack;無法在多個紋理集間實例化位圖
* &amp;lbrack;Viewport&amp;rbrack; 在有平鋪 UV 的網格上繪製時，刷新不完整
* &amp;lbrack;Iray&amp;rbrack;介電層會套用兩次法線貼圖
* &amp;lbrack;Shelf&amp;rbrack;某些Substance參數（alpha、程序式及素材素材）中的打字錯誤
* &amp;lbrack;Shelf&amp;rbrack;位圖「僅限授權人員」的打字錯誤
* &amp;lbrack;Script&amp;rbrack; 函式 alg.shaders.materials（） 已無法運作

**已知問題：**

* AMD VEGA GPU 的計算凍結問題

### 4.1.1 (2018.1.1)

*（發行日期：2018年4月3日）*

**修正：**

* &amp;lbrack;Tablet&amp;rbrack;更改預設互動選項時的問題
* &amp;lbrack;Bakers&amp;rbrack;與 Assimp 函式庫的崩潰
* &amp;lbrack;Bakers&amp;rbrack;與 A.O. 映射的效能迴歸分析
* &amp;lbrack;Iray&amp;rbrack;鏡頭失真不適用於 Alpha 通道
* &amp;lbrack;驅動程式&amp;rbrack;最低驅動程式要求更新
* &amp;lbrack;3Dview&amp;rbrack;沒有法線資訊的 UDIM 網格上法線無法正確產生
* &amp;lbrack;Intel&amp;rbrack;與Substance Painter 2018.1.0 的碰撞
* &amp;lbrack;Intel&amp;rbrack;&amp;lbrack;Viewport&amp;rbrack; 填充問題（黑色雜訊）

**已知問題：**

* AMD VEGA GPU 的計算凍結問題

### 4.1.0 (2018.1.0)

*（發行日期：2018年3月15日）*

**補充：**

* 全新整體風格（圖示、顏色、行為）
* 新的預設佈局
* &amp;lbrack;平板與布rack;繪畫時的使用者體驗提升
* &amp;lbrack;主選單&amp;rbrack;先在檢視和工具列中排序原生項目
* &amp;lbrack;主選單&amp;rbrack; 移動視口區段中的快速遮罩動作
* &amp;lbrack;主選單&amp;rbrack; 將右鍵點擊動作移至視窗區塊
* &amp;lbrack;主選單&amp;rbrack;將「檢視」選單重新命名為「視窗」
* &amp;lbrack;快速選單&amp;rbrack;在視窗中右鍵點擊新增工具屬性
* &amp;lbrack;Dock widget&amp;rbrack;新增用於快速減量/調回的工具列
* &amp;lbrack;顯示設定&amp;rbrack;攝影機與檢視器設定視窗合併
* &amp;lbrack;Layer stack&amp;rbrack; 上下文右鍵選單
* &amp;lbrack;Layer stack&amp;rbrack;拖放即可移動同一層內的任何效果
* &amp;lbrack;工具列與新情境工具列的重組
* &amp;lbrack;工具列&amp;rbrack; 將複製工具拆分成兩個獨立工具
* &amp;lbrack;工具屬性&amp;rbrack; 預覽中較淺的背景灰階值
* &amp;lbrack;工具屬性&amp;rbrack;分頁中的組織（填充與工具）
* &amp;lbrack;工具&amp;rbrack;上色結果與模板相符
* &amp;lbrack;Viewport&amp;rbrack;填充層的新游標
* &amp;lbrack;視窗&amp;rbrack;更流暢的導航與繪製（更高的幀率）
* &amp;lbrack;Viewport&amp;rbrack; viewport中的材質/通道/地圖組合選擇框
* &amp;lbrack;視窗&amp;rbrack;減少旋轉時的閃爍（陰影開啟）
* &amp;lbrack;Shelf&amp;rbrack;開啟 Painter 時預設顯示材料
* &amp;lbrack;Shelf&amp;rbrack;物質材質的載入時間改進（快2到6倍）
* &amp;lbrack;Shelf&amp;rbrack;重新整理材料資料夾以符合物質來源結構
* &amp;lbrack;Shelf&amp;rbrack;直接拖放材質到視窗的網格上
* &amp;lbrack;Shelf&amp;rbrack;新3D聲音（Perlin、Perlin分形、單純形與Worley）
* &amp;lbrack;Shelf&amp;rbrack;利用網格位置的新型3D線性梯度遮罩產生器
* &amp;lbrack;Shelf&amp;rbrack;更新底音以支援非平方展開
* &amp;lbrack;Shelf&amp;rbrack;新增了 Lens Studio（Snap 應用程式）的模板與匯出預設
* &amp;lbrack;Shelf&amp;rbrack;更新智慧材料與智慧口罩以使用最新版本的口罩編輯器（微細節）
* &amp;lbrack;Shelf&amp;rbrack;全新範例專案「TilingMaterial」，旨在創造無縫的拼貼材質
* &amp;lbrack;Shelf&amp;rbrack;新筆刷預設（書法、濕筆、陰影等）
* &amp;lbrack;滑桿與新滑桿與灰階/色條、風格與行為
* &amp;lbrack;Bakers&amp;rbrack;允許使用完整場景邊界框來計算位置圖
* &amp;lbrack;Shader&amp;rbrack; 從預設著色器參數中移除高度力參數
* &amp;lbrack;引擎&amp;rbrack;物質引擎更新
* &amp;lbrack;引擎&amp;rbrack;UV區塊間不連續或較少
* &amp;lbrack;Plugins&amp;rbrack;更快匯入從 Substance Source 下載的素材
* &amp;lbrack;Plugins&amp;rbrack; 更新所有插件以符合新的整體風格
* &amp;lbrack;偏好設定&amp;rbrack;預覽背景顏色自動更換
* &amp;lbrack;清潔與brack;降低專案貪腐風險
* &amp;lbrack;Open&amp;rbrack;開幕專案時間改善
* &amp;lbrack;新專案&amp;rbrack;新專案 - 網格更新時間改進
* &amp;lbrack;節省&amp;rbrack;節省專案時間改進
* &amp;lbrack;Log&amp;rbrack;授權類型以日誌報告
* &amp;lbrack;TextureSet&amp;rbrack; 將「烘焙材質」按鈕重新命名為「烘焙網格貼圖」
* 將「額外地圖」重新命名為「網格地圖」

**修正：**

* &amp;lbrack;Viewport&amp;rbrack;包含大量子物件的網格表現不佳
* &amp;lbrack;工具屬性&amp;rbrack;拖放圖片到材質槽時，通道被禁用
* &amp;lbrack;工具屬性&amp;rbrack;畫筆預覽因模糊與複製工具而失效
* &amp;lbrack;Texture set&amp;rbrack;使用模板時通道順序錯誤
* &amp;lbrack;Shelf&amp;rbrack;缺少灰階轉換產生器的圖示
* &amp;lbrack;Shelf&amp;rbrack;符號圈 數字 alpha 壞掉了（字體缺失）
* 上市時對整合 GPU 的錯誤偵測
* &amp;lbrack;Crash&amp;rbrack;拖放一個名為 # 字元的匯入資源
* &amp;lbrack;引擎與 rbrack;整合 GPU 的 VRAM 偵測問題
* &amp;lbrack;Engine&amp;rbrack;在《Substance Engine Linker》中修正了多起車禍
* &amp;lbrack;Engine&amp;rbrack;更改解析度時出現方形雜訊
* &amp;lbrack;後期效果&amp;rbrack;開啟後期效果時介面大小調整速度較慢
* &amp;lbrack;Bakers&amp;rbrack;場景單元並未正確尊重光線距離值
* &amp;lbrack;Bakers&amp;rbrack;AO 從網格遮蔽距離被夾為 1，不論輸入值為何
* &amp;lbrack;Bakers&amp;rbrack;以名稱匹配會忽略部分帶有特定名稱的網格
* &amp;lbrack;Bakers&amp;rbrack;從網格多元組和子網格 ID 設定中取得的顏色總是回傳黑色影像
* &amp;lbrack;Bakers&amp;rbrack;ID 烘焙在 Blender 的二進位 FBX 網格下失敗
* &amp;lbrack;著色器&amp;rbrack;使用 dota-2 及非 PBR 規格光澤的 2D 視圖噪點
* &amp;lbrack;Linux&amp;rbrack;烘焙時只使用一個 CPU 執行緒
* &amp;lbrack;MacOS&amp;rbrack;刷子游標移動於視窗上方時當機

**已知問題：**

* AMD VEGA GPU 的計算凍結問題
* 在 IRay（alpha）匯出時未考慮扭曲後製處理

## 版本 3

### 3.4.2 (2017.4.2)

*（發行日期：2018年1月24日）*

**補充：**

* &amp;lbrack;Export&amp;rbrack;取得出口狀態及步驟進度
* &amp;lbrack;Export&amp;rbrack; 允許取消出口
* &amp;lbrack;Export&amp;rbrack;將貼圖匯出到 Sketchfab，且不會損失法線貼圖品質
* &amp;lbrack;Export&amp;rbrack; 以 glTF 二進位格式（glb）匯出
* &amp;lbrack;Export&amp;rbrack;允許在匯出視窗的設定標籤中調整欄位大小
* &amp;lbrack;Shader&amp;rbrack; 新增著色器 API 的變更日誌
* &amp;lbrack;Scripting&amp;rbrack;在匯出貼圖時加入前後回調函數
* &amp;lbrack;Iray&amp;rbrack;升級至 SDK 2017.1（支援 Volta GPU）

**修正：**

* 在主視窗顯示前退出應用程式時會當機
* &amp;lbrack;MAC&amp;rbrack;載入灰階地圖時 IRAY 當機
* &amp;lbrack;MAC&amp;rbrack;新 High Sierra OS 的 VRAM 偵測不正確
* &amp;lbrack;Plugin&amp;rbrack; 從 Substance Source 下載資產已無法使用
* &amp;lbrack;Scripting&amp;rbrack;錯誤的最小插件版本偵測
* &amp;lbrack;Export&amp;rbrack; 匯出材質後無法儲存匯出預設
* &amp;lbrack;Instancing&amp;rbrack; 關於在無額外貼圖的 TextureSet 中實例化的產生器問題
* &amp;lbrack;Viewport&amp;rbrack;抖動在解析度超過 4k 時無法運作
* &amp;lbrack;視窗&amp;rbrack;2D 視圖材質顯示被雜訊覆蓋
* &amp;lbrack;Shelf&amp;rbrack;提升架上預設的載入時間
* &amp;lbrack;Engine&amp;rbrack;在色彩選擇下繪製時混合不正確

### 3.4.1 (2017.4.1)

*（發行日期：2017年12月15日）*

**補充：**

* &amp;lbrack;Scripting&amp;rbrack; 透過腳本 API 匯出網格
* &amp;lbrack;Import&amp;rbrack;停用不支援的網狀檔案格式匯入（僅允許 obj、fbx、dae、ply）
* &amp;lbrack;Log&amp;rbrack;更精確地指示日誌檔中的TDR問題

**修正：**

* 如果應用程式在資源爬取完成前關閉，就會當機
* 使用 Smudge/Clone 工具開啟專案時會當機
* 在檢視器設定中還原著色器變更後，使用重做時會當機
* &amp;lbrack;Engine&amp;rbrack;材質在 Painter 2017.2 與 2017.4 之間有所不同
* &amp;lbrack;Viewport&amp;rbrack; 從實例中選取 ID 映射會取樣錯誤的顏色
* &amp;lbrack;Export&amp;rbrack;匯出無效法線或遮蔽材質時會當機
* &amp;lbrack;Export&amp;rbrack;PSD 檔案在 Photoshop CS6 開啟時群組會被鎖定
* &amp;lbrack;Plugin&amp;rbrack;Photoshop 外掛會忽略頻道選擇，並且總是匯出所有內容
* &amp;lbrack;Layers&amp;rbrack;錨點在複製/貼上於貼圖集時會斷裂
* &amp;lbrack;Layers&amp;rbrack;有些錨點的參考若被破壞無法恢復
* &amp;lbrack;Shader&amp;rbrack;pbr塗層的次級粗糙度參數被破壞
* &amp;lbrack;Steam&amp;rbrack;版本檢查器彈出視窗在啟動時不應該顯示

**已知問題：**

* &amp;lbrack;AMD&amp;rbrack;嘗試在網格上繪製時會當機/凍結。 可以透過更新顯示卡驅動程式來解決。

### 3.4.0 (2017.4.0)

*（發行日期：2017年11月23日）*

**補充：**

* &amp;lbrack;Instancing&amp;rbrack; 允許跨層實例化參數
* &amp;lbrack;Instancing&amp;rbrack;允許在來源層與實例間跳轉
* &amp;lbrack;Instancing&amp;rbrack; 新增「跨材質集實例化」動作
* &amp;lbrack;Instancing&amp;rbrack;在層堆疊中表示重入實例（週期數）
* &amp;lbrack;Instancing&amp;rbrack;當來源被移除時刪除實例
* &amp;lbrack;Instancing&amp;rbrack;不允許 Anchor 從實例資料夾外的引用
* &amp;lbrack;UI&amp;rbrack;將復原堆疊移入名為「歷史」的獨立視窗
* &amp;lbrack;Plugin&amp;rbrack; 整合 DCC 即時連結插件
* &amp;lbrack;Engine&amp;rbrack;用稀疏塗裝提升繪畫效能
* &amp;lbrack;Export&amp;rbrack;為 Sketchfab 匯出器新增草圖與重新匯出選項
* &amp;lbrack;Shelf&amp;rbrack; 新增字型物質的「翻轉」控制
* &amp;lbrack;Shelf&amp;rbrack;新增20個程序性材料
* &amp;lbrack;Shelf&amp;rbrack; 新增 40 張 grunges 地圖（基於點陣圖與程序生成）
* &amp;lbrack;Viewport&amp;rbrack;啟用其他可見材質集的筆刷預覽碰撞
* 更新 AMD GPU 驅動程式的最低需求

**修正：**

* 當以過高解析度計算物質時會崩潰
* 大量粉粒上色時會發生崩潰
* &amp;lbrack;Viewport&amp;rbrack; 在特定網格下 2D 視圖中鏡面反射錯誤
* &amp;lbrack;UI&amp;rbrack;部分不想要的動作會出現在歷史視窗中

**已知問題：**

* &amp;lbrack;Layers&amp;rbrack;有些錨點的參考若被破壞無法恢復
* 在檢視器設定中還原著色器變更後，使用重做時會當機

### 3.3.3 (2017.3.3)

*（發行日期：2017年12月1日）*

**修正：**

* &amp;lbrack;Steam&amp;rbrack;版本檢查器彈出視窗在啟動時不應該顯示
* &amp;lbrack;Export&amp;rbrack;PSD 檔案在 Photoshop CS6 開啟時群組會被鎖定

### 3.3.2 (2017.3.2)

*（發行日期：2017年11月20日）*

**補充：**

* &amp;lbrack;UI&amp;rbrack;改進新版本對話框並新增變更日誌
* &amp;lbrack;UI&amp;rbrack;在新版本對話框中指示維護是否已過期
* &amp;lbrack;License&amp;rbrack;更新授權系統以處理維護日期
* &amp;lbrack;Export&amp;rbrack;將 Adobe 標準材料重新命名為 Adobe Dimension

**修正：**

* &amp;lbrack;Mac&amp;rbrack;繪畫會導致黑色方格和紋理損壞
* &amp;lbrack;Engine&amp;rbrack;快取有時會在視窗中消失
* &amp;lbrack;Engine&amp;rbrack;當記憶體壓縮觸發時會出現方塊狀的雜訊
* &amp;lbrack;Baking&amp;rbrack;烘焙特定網格時會出現奇怪的錯誤訊息
* &amp;lbrack;Export&amp;rbrack;PSD 寫法錯誤，Photoshop 無法正確辨識
* &amp;lbrack;Layers&amp;rbrack;理論上不可能複製/貼上圖層跨多個專案
* &amp;lbrack;Substance&amp;rbrack;UserData 的 Normal 輸入色彩空間在某些情況下會被翻轉
* &amp;lbrack;Shelf&amp;rbrack;產生器中微正規化輸出反曲率
* &amp;lbrack;Shelf&amp;rbrack;HSL 濾波器也會影響 alpha 通道
* &amp;lbrack;Linux&amp;rbrack;在 CentOS 上安裝失敗，因為缺少相依
* 安裝程式在某些情況下不會移除之前安裝的所有資源

### 3.3.1 (2017.3.1)

*（發行日期：2017年10月26日）*

**補充：**

* &amp;lbrack;Export&amp;rbrack; 允許從專案匯出網格
* &amp;lbrack;Shelf&amp;rbrack;將分頁標題中的「Sub-Shelf」移除
* 將後製程設定儲存在範本中
* 讓TDR訊息更易理解
* 改善設定視窗以回報錯誤

**修正：**

* 刪除多個子層架時會當機
* 在引擎計算過程中從關卡切換到其他關卡時會當機
* &amp;lbrack;Mac&amp;rbrack;Intel GPU 引擎運算時當機
* &amp;lbrack;Mac&amp;rbrack;&amp;lbrack;Viewport&amp;rbrack; 啟用抖動時表現不佳
* &amp;lbrack;Mac&amp;rbrack;MacOS 10.13 在日誌檔中被識別為「未知版本」
* &amp;lbrack;Baker&amp;rbrack;用籠子烤已經不行了
* &amp;lbrack;Layers&amp;rbrack;Ctrl + C 快捷鍵（複製動作）已經無法使用
* &amp;lbrack;Layers&amp;rbrack;貼圖層不會刷新帶有錨點參考的 UI
* &amp;lbrack;Anchor&amp;rbrack; 重複或複製/貼上帶有參考的圖層會斷開連結
* &amp;lbrack;Export&amp;rbrack;8K 匯出在某些情況下可能會當機或死結應用程式
* &amp;lbrack;Export&amp;rbrack;生成的 glTF 檔案格式出現多個問題
* &amp;lbrack;Import&amp;rbrack;重新匯入相同檔名的網格已經無法再運作了
* &amp;lbrack;Plugin&amp;rbrack;自動存檔視窗總是會出現在所有東西的上方
* &amp;lbrack;UI&amp;rbrack;在TDR對話框按下「Esc」時的無限迴圈
* &amp;lbrack;UI&amp;rbrack; 重置 UI 在書架視窗顯示第二個標題列

### 3.3.0 (2017.3.0)

*（發行日期：2017年9月28日）*

**補充：**

* &amp;lbrack;Export&amp;rbrack;允許匯出 Adobe Project Felix 的網格與材質
* &amp;lbrack;Export&amp;rbrack; 允許匯出為 glTF 檔案格式
* &amp;lbrack;Engine&amp;rbrack;透過區塊壓縮優化 VRAM 中的貼圖大小
* &amp;lbrack;Viewport&amp;rbrack;能夠在視窗中拖放網格或專案
* &amp;lbrack;UI&amp;rbrack; 改進關於 TDR 的警告訊息
* &amp;lbrack;UI&amp;rbrack; 日誌應僅在請求時顯示
* &amp;lbrack;UI&amp;rbrack; 允許清除日誌視窗的內容
* &amp;lbrack;UI&amp;rbrack;在狀態列中顯示警告與錯誤
* &amp;lbrack;UI&amp;rbrack;顯示分頁在頂部，與網頁瀏覽器相同
* &amp;lbrack;UI&amp;rbrack; 改善「不可塗裝」的上下文與訊息
* &amp;lbrack;UI&amp;rbrack;在檔案選單中新增「另存為複製」動作
* &amp;lbrack;Layer&amp;rbrack;預設將平鋪設定設為 1
* &amp;lbrack;Shelf&amp;rbrack;改良漸層濾鏡，支援10種動態色彩
* &amp;lbrack;Shelf&amp;rbrack;在迷你書架的預設查詢中加入空格
* &amp;lbrack;Shelf&amp;rbrack;新增「在瀏覽器中開啟」的本地資源操作
* &amp;lbrack;Shelf&amp;rbrack;新增 Adobe Material Standard（Project Felix）的模板與著色器
* &amp;lbrack;Shelf&amp;rbrack;將最大平鋪增加到 128 吋材質層疊著色器
* &amp;lbrack;Shelf&amp;rbrack;新增 sobel 曲率以顯示掩模產生器的微細細節
* &amp;lbrack;Plugin&amp;rbrack; 新增可自訂時間間隔的自動儲存插件
* &amp;lbrack;Scripting&amp;rbrack; 新增「另存為複製」功能

**修正：**

* &amp;lbrack;UI&amp;rbrack;版面在首次啟動時就壞掉了
* &amp;lbrack;Export&amp;rbrack; 匯出時產生的 PSD 格式錯誤
* &amp;lbrack;Export&amp;rbrack;EXR 總是匯出 8 位元高度圖
* &amp;lbrack;Export&amp;rbrack;匯出損壞後會當機 額外地圖
* &amp;lbrack;Import&amp;rbrack;在某些情況下，低多邊形網格上不會保留硬邊
* &amp;lbrack;Import&amp;rbrack;在匯入有問題的網格時，改進錯誤訊息
* &amp;lbrack;Bakers&amp;rbrack; ID 地圖烘焙失敗，啟用「按姓名配對」
* &amp;lbrack;Viewport&amp;rbrack;切線空間與 bakers 不同步
* &amp;lbrack;Effect&amp;rbrack;往後移動一層不會恢復錨點的參考
* &amp;lbrack;Effect&amp;rbrack; 在兩個 Mask 與 anchors 之間建立連結時的刷新問題
* &amp;lbrack;Effect&amp;rbrack;遮罩上方的 Masks 錨點不應該被列出
* &amp;lbrack;Effect&amp;rbrack; 從 Anchors 擷取 Alpha 設定無法運作
* &amp;lbrack;引擎&amp;rbrack;面罩在第一次刷筆劃後會倒轉
* &amp;lbrack;Engine&amp;rbrack;在特定專案切換材質集時會當機
* &amp;lbrack;Shelf&amp;rbrack;刪除專案中的預設時會當機
* &amp;lbrack;Shelf&amp;rbrack;進階三平面濾波器中的打字錯誤
* &amp;lbrack;Shelf&amp;rbrack;MG 面罩建構器 AO 噪音音階無法正常運作
* &amp;lbrack;Shelf&amp;rbrack;MG 面罩建構器具有反轉曲率參數
* &amp;lbrack;Shelf&amp;rbrack;匯入的 alpha 會產生材質球體預覽，而非平面預覽

### 3.2.0 (2017.2.0)

*（發行日期：2017年7月27日）*

**補充：**

* 錨點 - 圖層與遮罩參照系統
* &amp;lbrack;Layers&amp;rbrack; 可重新命名填充與繪畫效果
* &amp;lbrack;Plugin&amp;rbrack; 更新的 Substance Source 插件
* &amp;lbrack;Scripting&amp;rbrack; 允許查詢紋理集解析
* &amp;lbrack;Scripting&amp;rbrack; 允許取得繪製引擎的狀態
* &amp;lbrack;效能&amp;rbrack;改進專案載入與刷刷沖壓優化

**修正：**

* &amp;lbrack;工具&amp;rbrack;調整材料參數時的效能問題
* &amp;lbrack;Engine&amp;rbrack;解析度變更時筆觸消失（4K>2K）
* &amp;lbrack;3D View&amp;rbrack;切線空間不會與 Baker 同步
* &amp;lbrack;Shelf&amp;rbrack;使用者文件中的架子路徑不會自動建立
* &amp;lbrack;Shelf&amp;rbrack;更新後讓預設與先前版本相容
* &amp;lbrack;著色器&amp;rbrack;非 PBR 著色器不再運作
* &amp;lbrack;Bakers&amp;rbrack; ID 地圖烘焙失敗，啟用「按姓名配對」
* &amp;lbrack;Sample&amp;rbrack; Meet Mat 範例專案 材質集名稱不正確
* 在建立範本前儲存專案會回傳寫入權限錯誤

### 3.1.0 (2017.1.0)

*（發行日期：2017年6月20日）*

**補充：**

* &amp;lbrack;Plugin&amp;rbrack;新的 Substance Source 外掛（允許下載書架上的資產）
* &amp;lbrack;Shelf&amp;rbrack;4 種新字體（日文 + 簡體中文，打字機，分段）
* &amp;lbrack;Shelf&amp;rbrack;230 個新 Alpha（圖案、畫筆與指紋掃描混合）
* &amp;lbrack;Shelf&amp;rbrack;50 部新程序劇（中世紀與當代服裝的布料圖案）
* &amp;lbrack;書架與 2 張新環境地圖（Mondarrain 與 Villa Nova 街）
* &amp;lbrack;Shelf&amp;rbrack;9 個新濾鏡（MatFx Detail Edge Wear、Clamp、HBAO 等）
* &amp;lbrack;Shelf&amp;rbrack;改良的預設全景環境地圖
* &amp;lbrack;Shelf&amp;rbrack;新 Arnold 5 匯出預設
* &amp;lbrack;Scripting&amp;rbrack; 允許將資源匯入書架

**已知問題：**

* &amp;lbrack;Export&amp;rbrack;編輯匯出預設非常慢

## 版本 2

### 2.6.2

*（發行日期：2017年10月20日）*

**補充：**

* &amp;lbrack;Texture Set&amp;rbrack; 允許刪除已停用的材質集
* &amp;lbrack;Shelf&amp;rbrack;允許多個使用者在同一個 shelf 資料夾內書寫
* &amp;lbrack;Scripting&amp;rbrack; 能夠重新載入插件資料夾
* &amp;lbrack;Scripting&amp;rbrack;在外掛元資料中加入必要的最低 API 版本以確保相容性
* &amp;lbrack;IRay&amp;rbrack;輸出影像對話改進

**修正：**

* &amp;lbrack;Engine&amp;rbrack;在改變解析度（4K>2K）時，筆劃消失的問題
* &amp;lbrack;Bakers&amp;rbrack; ID 地圖烘焙失敗，啟用「按姓名配對」
* &amp;lbrack;Bakers&amp;rbrack;錯誤訊息不夠明確
* &amp;lbrack;3D View&amp;rbrack;切線空間不會與 Baker 同步
* &amp;lbrack;工具&amp;rbrack;使用污漬工具時出現黑色雜訊
* &amp;lbrack;著色器&amp;rbrack;非 PBR 著色器不再運作
* &amp;lbrack;Shader&amp;rbrack;「PBR塗層」是壞掉的
* &amp;lbrack;著色器與塗層：塗層 「pbr 塗層」著色器的粗糙度不再影響
* &amp;lbrack;著色器&amp;rbrack;規格光澤著色器與 Iray 和 SD 不匹配
* &amp;lbrack;Shelf&amp;rbrack;載入兩個同名但副檔名不同的檔案時會當機
* &amp;lbrack;Shelf&amp;rbrack;無法再編輯書架上的預設
* &amp;lbrack;Shelf&amp;rbrack;無法為匯入在書架上的資產設定自訂預覽
* 從快取載入的資源會失去使用量
* 在建立範本前儲存專案會回傳寫入權限錯誤
* 如果檔名包含兩個週期，則是錯誤的專案儲存
* 匯入多點檔案（.） 檔名會造成問題

### 2.6.1

*（發行日期：2017年5月12日）*

**補充：**

* &amp;lbrack;TextureSet&amp;rbrack; 不允許將網格材質重新分配到零

**修正：**

* 更換烘焙貼圖後切換 TextureSet 時會當機
* 在更換圖層混合模式後，執行「復原與重做」時會當機
* 使用「色彩選擇」效果搭配大 ID 映射時會當機或凍結
* &amp;lbrack;Export&amp;rbrack;已命名的材質集在匯出視窗中並未按字母順序排序
* &amp;lbrack;TextureSet&amp;rbrack; 重置為預設名稱不會檢查統一性
* &amp;lbrack;TextureSet&amp;rbrack;重新命名的紋理集在重新開啟專案後會被停用
* &amp;lbrack;Shelf&amp;rbrack;缺少預設範本內容
* &amp;lbrack;Shelf&amp;rbrack;非正方形的貼圖則以正方形顯示
* &amp;lbrack;Shader&amp;rbrack;一旦一個貼圖集被禁用，相關的著色器就會被銷毀
* &amp;lbrack;Scripting&amp;rbrack; alg.baking.setTextureSetBakingParameters（） 已經無法運作了
* &amp;lbrack;腳本&amp;rbrack;websocket教學中的錯字
* &amp;lbrack;腳本&amp;rbrack;AlgWidgets 中的各種問題
* &amp;lbrack;Log&amp;rbrack;在某些情況下錯誤偵測可用虛擬記憶體

### 2.6.0

*（發行日期：2017年4月27日）*

**補充：**

* 新增範例專案「Meet Mat」
* &amp;lbrack;Plugin&amp;rbrack;新的「資源更新器」外掛
* &amp;lbrack;TextureSet&amp;rbrack; 允許重新命名並新增紋理集的描述
* &amp;lbrack;TextureSet&amp;rbrack; 允許重新分配材質
* &amp;lbrack;TextureSet&amp;rbrack; 在材質集列表視窗中新增設定按鈕
* &amp;lbrack;TextureSet&amp;rbrack; 在列表底部顯示「停用」的紋理集
* &amp;lbrack;Substance&amp;rbrack;使用目前材質集解析度的額外貼圖以提升效能
* &amp;lbrack;Scripting&amp;rbrack;允許更新專案中使用的資源（材料、產生器等）
* &amp;lbrack;Scripting&amp;rbrack; 新增或移除書架的方式
* &amp;lbrack;腳本&amp;rbrack;允許查詢專案中資源資訊
* &amp;lbrack;Scripting&amp;rbrack; 允許檢索可用書架清單
* &amp;lbrack;Scripting&amp;rbrack; 改進 AlgWidget 縮圖教學
* &amp;lbrack;Export&amp;rbrack;根據檔案格式支援啟用/啟用位元深度
* &amp;lbrack;Log&amp;rbrack; 在主控台中新增外掛名稱以列印
* &amp;lbrack;Log&amp;rbrack; 移除關於隱藏材質集的錯誤
* 更新「歡迎畫面」，加入新的圖示和文字範例

**修正：**

* 在特定專案更新網格時會當機
* &amp;lbrack;視窗&amp;rbrack;對稱平面內色不再可見
* &amp;lbrack;Viewport&amp;rbrack;使用單一視圖時會啟用部分後製處理效果
* &amp;lbrack;Shaders&amp;rbrack;「over_premult」混合無法正常運作
* &amp;lbrack;Shaders&amp;rbrack; 關於預設著色器 alpha 測試的警告
* &amp;lbrack;Shelf&amp;rbrack;錯誤解析 Substances 標籤
* &amp;lbrack;Shelf&amp;rbrack;MatFX 防鏽老化無法正常運作
* &amp;lbrack;Shelf&amp;rbrack;HSL 過濾器預設會啟用於錯誤頻道
* &amp;lbrack;Shelf&amp;rbrack;Sharpen 預設在 Height/Normal 通道啟用
* &amp;lbrack;Export&amp;rbrack;Vray 匯出預設不使用 OpenGL 法線貼圖
* &amp;lbrack;Tool&amp;rbrack;複製/污漬工具的不精確問題會產生雜訊

### 2.5.3

*（發行日期：2017年3月15日）*

**修正：**

* &amp;lbrack;Baker&amp;rbrack;用特定網格烘焙時會崩潰

**已知問題：**

* &amp;lbrack;Mac&amp;rbrack;粒子在某些情況下會造成材質損毀

### 2.5.2

*（發行日期：2017年3月14日）*

**修正：**

* &amp;lbrack;Tool&amp;rbrack;Wacom 繪圖板無法在 Linux 上運作
* &amp;lbrack;工具&amp;rbrack;使用污漬工具時出現黑色雜訊
* &amp;lbrack;Bakers&amp;rbrack;若使用「Match By Name」與籠子，烘焙失敗
* &amp;lbrack;Bakers&amp;rbrack;僅用法線貼圖烘焙時環境遮蔽失效
* &amp;lbrack;Shelf&amp;rbrack;通用濾波器無法妥善處理 alpha（對比度/亮度、高通濾波器等）
* &amp;lbrack;Viewport&amp;rbrack;啟用陰影時載入專案時的效能問題
* &amp;lbrack;Viewport&amp;rbrack;MacOS 3D 檢視中的抖動問題
* &amp;lbrack;Viewport&amp;rbrack;啟用色彩設定檔時，粒子預覽顯示錯誤
* &amp;lbrack;Iray&amp;rbrack;若 Iray 未初始化，將專案切回 OpenGL 時當機
* &amp;lbrack;IRay&amp;rbrack;在渲染 SpecGloss shader/mdl 時，光澤度會被忽略
* &amp;lbrack;Shader&amp;rbrack;Spec/Gloss shader 不匹配 Iray 和 SD
* &amp;lbrack;Shader&amp;rbrack;sRGB 轉換與線性轉為 sRGB LUT 的差異
* &amp;lbrack;Shader&amp;rbrack;載入專案時使用過時著色器顯示不正確
* &amp;lbrack;Shader&amp;rbrack;「PBR 塗層」著色器已經無法使用了
* &amp;lbrack;Export&amp;rbrack;即使不存在於材質集中，有些通道仍會被匯出
* &amp;lbrack;Layers&amp;rbrack; 混合模式「法線貼圖反向細節」在灰階通道上無法運作
* &amp;lbrack;UI&amp;rbrack;在 HDPI 螢幕與顯示縮放到 150% 時，「色彩選擇視窗」的問題

**已知問題：**

* &amp;lbrack;Mac&amp;rbrack;粒子在某些情況下會造成材質損毀

### 2.5.1

*（發行日期：2017年2月27日）*

**修正：**

* &amp;lbrack;Mac&amp;rbrack;Wacom 繪圖板輸入在 3D 與 2D 視圖中斷裂
* &amp;lbrack;Bakers&amp;rbrack;以名字匹配已無法再行
* &amp;lbrack;Bakers&amp;rbrack;「平均法線」設定不再有效
* &amp;lbrack;Iray&amp;rbrack;缺乏烘焙法線貼圖的錯誤渲染
* &amp;lbrack;Iray&amp;rbrack;色彩設定檔與 OpenGL 渲染器相比表現不同
* &amp;lbrack;Iray&amp;rbrack;匯出渲染為點陣圖時不包含色彩配置校正
* &amp;lbrack;Substance&amp;rbrack;材質過濾器不再運作了
* &amp;lbrack;Tool&amp;rbrack;筆劃不透明度不會儲存在筆刷預設中
* &amp;lbrack;工具&amp;rbrack;複製刷子的 UV 對齊功能不再運作
* &amp;lbrack;Export&amp;rbrack;位移通道在整數匯出時應置中為 0.5
* &amp;lbrack;Template&amp;rbrack;絕對路徑儲存在 Templates 中
* &amp;lbrack;TextureSet&amp;rbrack;移除通道後，通道紋理仍會持續存在

**已知問題：**

* &amp;lbrack;Linux&amp;rbrack;Wacom 繪圖板的輸入在 3D 和 2D 視圖中都無法使用
* &amp;lbrack;Mac&amp;rbrack;粒子在某些情況下會造成材質損毀
* &amp;lbrack;Export&amp;rbrack;在極少數情況下，AMD GPU 上會出現黑色矩形

### 2.5.0

*（發行日期：2017年2月21日）*

**補充：**

* 新增對 AMD Radeon Pro 和 AMD FirePro GPU 的支援
* &amp;lbrack;Tool&amp;rbrack; 新增筆劃不透明度支援
* &amp;lbrack;Tool&amp;rbrack;新增一個修飾符，允許繼續上一次筆觸
* &amp;lbrack;Iray&amp;rbrack;更新以支援 Pascal GPU
* &amp;lbrack;Viewport&amp;rbrack; 新增對色彩設定檔（LUT）的支援
* &amp;lbrack;Substance&amp;rbrack;整合新框架（SD6引擎）
* &amp;lbrack;UI&amp;rbrack; 在檔案選單中增加「近期檔案」大小列表
* &amp;lbrack;Import&amp;rbrack; 使用 substics 的類別來填補匯入對話框中的前綴
* &amp;lbrack;Bakers&amp;rbrack;允許烘焙 8K 紋理
* &amp;lbrack;Bakers&amp;rbrack;允許烘焙非正方形解析度
* &amp;lbrack;Bakers&amp;rbrack;烘焙重高多邊形網格時提升記憶體消耗
* &amp;lbrack;Shelf&amp;rbrack;鎖定書架（及專案），禁止同時編輯並避免損壞
* &amp;lbrack;Shelf&amp;rbrack;從物質中讀取分類和關鍵字，以便進行篩選
* &amp;lbrack;Shelf&amp;rbrack;允許將資源排除在搜尋查詢結果之外
* &amp;lbrack;Shelf&amp;rbrack;改進縮圖時間計算
* &amp;lbrack;Shelf&amp;rbrack;允許在專案中嵌入預設
* &amp;lbrack;Shelf&amp;rbrack;允許使用 SHIFT 快速摺疊/展開樹狀圖
* &amp;lbrack;Shelf&amp;rbrack;允許在資產只讀時儲存縮圖（本地快取）
* &amp;lbrack;Shelf&amp;rbrack;新內容：新增濾鏡（transform、mirror、tri-planear 等）
* &amp;lbrack;Shelf&amp;rbrack;新內容：新的 LUT 設定檔（經典與藝術風格，如黑色電影、復古等）
* &amp;lbrack;Shelf&amp;rbrack; 新內容：10 種新字體材質，可快速生成自訂文本
* &amp;lbrack;Shelf&amp;rbrack;新模板：Unity 5 與 Unreal Engine 4
* &amp;lbrack;Shelf&amp;rbrack;改良 HSL 濾鏡，使其更友善於藝術家
* &amp;lbrack;Shader&amp;rbrack;在 PBR 著色器中新增對鏡面關卡通道的支援
* &amp;lbrack;著色器&amp;rbrack;在 Alpha 測試著色器中新增抖動支援
* &amp;lbrack;Shader&amp;rbrack;在 PBR 著色器中新增視差遮蔽映射的支援
* &amp;lbrack;Shader&amp;rbrack; 允許定義著色器參數的自訂 UI
* &amp;lbrack;MatLayering&amp;rbrack;建立新的遮罩通道用於材質分層工作流程
* &amp;lbrack;Scripting&amp;rbrack;允許在 SP 專案中撰寫元資料
* &amp;lbrack;Scripting&amp;rbrack;允許以特定匯出預設匯出
* &amp;lbrack;Scripting&amp;rbrack; 允許以 JSON 格式取得著色器參數
* &amp;lbrack;腳本&amp;rbrack;新增對 WebSocket 連線的支援
* &amp;lbrack;Scripting&amp;rbrack; 新增載入著色器實例的可能性
* &amp;lbrack;腳本&amp;rbrack; 新增建立新專案的可能性
* &amp;lbrack;Scripting&amp;rbrack; 允許擷取專案中匯入網格的網址
* &amp;lbrack;腳本&amp;rbrack;允許非方形烘焙
* &amp;lbrack;Scripting&amp;rbrack;透過腳本 API 設定資料時回報錯誤
* &amp;lbrack;Substances&amp;rbrack; 新增使用者資料標籤以指定法線映射格式

**修正：**

* 用物質挑色時會崩潰
* 載入非 RGBA32f 影像作為環境貼圖時會當機
* 與 AMD GPU 上繪圖相關的當機
* &amp;lbrack;Mesh&amp;rbrack;OBJ 匯入無法辨識沒有 mtl 檔案的材質
* &amp;lbrack;Mesh&amp;rbrack; UDIM 材質集名稱的產生在某些網格上可能不正確
* &amp;lbrack;UI&amp;rbrack;檢視器設定中的復原/重做按鈕可偷走焦點並停止滑鼠捲動
* &amp;lbrack;UI&amp;rbrack;有些標籤在 High-DPI 中被錯誤裁切
* &amp;lbrack;Layer&amp;rbrack;替換模式用於繪圖效果，在遮罩上有錯誤行為
* &amp;lbrack;Layer&amp;rbrack; 減法混合模式在 alpha 時行為不正確
* &amp;lbrack;Tool&amp;rbrack;在 2D 視圖中，當在 UV 邊界上繪畫時，筆刷尺寸會變得非常巨大
* &amp;lbrack;工具&amp;rbrack;吸附直線在高DPI下行為不穩定
* &amp;lbrack;工具&amp;rbrack;模板解析度有時不正確
* &amp;lbrack;Bakers&amp;rbrack;「最大遮蔽距離」值若「相對於邊界框」為「關閉」則會被夾住
* &amp;lbrack;Shader&amp;rbrack;堆疊與自動參數通道定義不匹配
* &amp;lbrack;3D 視圖&amp;rbrack;根據專案設定，正常通道顯示不一致
* &amp;lbrack;Viewport&amp;rbrack;有些法線貼圖有壓縮值，會呈現為雜訊
* &amp;lbrack;Viewport&amp;rbrack;後製效果預設是被禁用的
* &amp;lbrack;Export&amp;rbrack;如果缺少正常通道，正常混音設定就是不正確的
* &amp;lbrack;Export&amp;rbrack;AMD GPU 在某些情況下出現錯誤的貼圖產生
* &amp;lbrack;Export&amp;rbrack;若著色器參數位於群組內，則無法正確匯出
* &amp;lbrack;Export&amp;rbrack; 在自訂架子中編輯匯出預設時會產生日誌錯誤
* &amp;lbrack;Shelf&amp;rbrack;樹狀檢視過濾與資料夾名稱不完全相符
* &amp;lbrack;Shelf&amp;rbrack;重新命名 shelf 預設很難辨認
* &amp;lbrack;Shelf&amp;rbrack;在重新推出後，從 Shelf 匯入的著色器資源不會被保存
* &amp;lbrack;Shelf&amp;rbrack;內容：缺少焊接工具預設
* &amp;lbrack;Shelf&amp;rbrack;內容：磁磚產生器無法正常運作
* &amp;lbrack;Shelf&amp;rbrack;內容：修正橡膠輪胎上的錯誤遮罩 骯髒的智慧材質
* &amp;lbrack;Shelf&amp;rbrack;內容：修正皮革包材上錯誤的團體名稱
* &amp;lbrack;Iray&amp;rbrack;Iray 中缺少一半的網格
* &amp;lbrack;Linux&amp;rbrack; 在 3D 檢視圖上方拖曳資源時會當機
* &amp;lbrack;Mac&amp;rbrack;偏好設定會在 Sierra 每次啟動時重置

**已知問題：**

* &amp;lbrack;Export&amp;rbrack;在極少數情況下，AMD GPU 上會出現黑色矩形
* &amp;lbrack;Iray&amp;rbrack;色彩設定檔有時會表現得很奇怪

### 2.4.1

*（發行日期：2016年10月28日）*

**修正：**

* 使用範本建立專案時會當機
* 在匯出過程中關閉匯出對話框時會當機
* &amp;lbrack;Mac&amp;rbrack;儲存專案時出現錯誤（匯出預設失敗）
* &amp;lbrack;Shelf&amp;rbrack;建立新預設會顯示兩次
* &amp;lbrack;Shelf&amp;rbrack;預設在沒有管理員權限的情況下無法以唯讀模式載入

### 2.4.0

*（發行日期：2016年10月27日）*

**補充：**

* &amp;lbrack;Shelf&amp;rbrack;新的介面用來瀏覽資源（樹狀檢視、篩選器等）
* &amp;lbrack;Shelf&amp;rbrack;允許將搜尋儲存為預設
* &amp;lbrack;Shelf&amp;rbrack; 允許從預設建立新視窗
* &amp;lbrack;Shelf&amp;rbrack;新介面用於匯入資源
* &amp;lbrack;Shelf&amp;rbrack;請勿在文件資料夾中複製預設的寓言書架
* &amp;lbrack;Shelf&amp;rbrack;新粒子預設：電路、電線、洛可可、小脈絡
* &amp;lbrack;Shelf&amp;rbrack;改良舊粒子預設，使其更易使用（如「Rain」）
* &amp;lbrack;Shelf&amp;rbrack;新增資源情境選單資訊
* &amp;lbrack;Viewport&amp;rbrack; 在載入環境地圖時提升效能
* &amp;lbrack;Viewport&amp;rbrack; 新增非二冪次方的環境地圖支援

**修正：**

* 摘下面罩時的撞擊聲
* 儲存預設後上色時當機
* 某些顯示卡會因環境模糊而當機
* 當用迷你架子指派錯誤資源時會當機
* &amp;lbrack;Shelf&amp;rbrack; Clean + 儲存 移除專案中資源的標籤與元資料
* &amp;lbrack;Shelf&amp;rbrack;匯入預設會在書架中顯示其資源
* &amp;lbrack;Export&amp;rbrack;從高度通道產生的法線貼圖強度較低
* &amp;lbrack;Export&amp;rbrack; 網格的法線不一定出現在最終法線貼圖中
* &amp;lbrack;Export&amp;rbrack;有時候透明的膨脹會導致完全沒有透明度
* &amp;lbrack;Scripting&amp;rbrack; “alg.plugin_root_directory” 可以回傳截斷的網路路徑
* &amp;lbrack;TextureSet&amp;rbrack;重新開啟非方形專案時會啟用鎖定按鈕

### 2.3.1

*（發行日期：2016年10月7日）*

**補充：**

* &amp;lbrack;Plugin&amp;rbrack;&amp;lbrack;Photoshop&amp;rbrack; 允許指定要匯出哪些材質/堆疊/通道
* &amp;lbrack;腳本&amp;rbrack;函式名稱存在一些不一致之處

**修正：**

* &amp;lbrack;Export&amp;rbrack;Alpha 可在自訂匯出預設中捨棄
* &amp;lbrack;Export&amp;rbrack;Alpha 在 sRGB 頻道上出現錯誤的伽瑪轉換
* &amp;lbrack;Export&amp;rbrack;非方形文件匯出為平方
* &amp;lbrack;Export&amp;rbrack;若缺少一張地圖，無法匯出額外地圖
* &amp;lbrack;Iray&amp;rbrack;有些參數（例如發射強度）沒有影響
* &amp;lbrack;NVIDIA&amp;rbrack;使用 NVIDIA Quadro K2200/GTX 750/760 啟動時當機
* &amp;lbrack;AMD&amp;rbrack;縮圖與預覽的顏色組合錯誤
* &amp;lbrack;AMD&amp;rbrack;新檔案與檔案開啟時當機與驅動程式故障
* &amp;lbrack;Log&amp;rbrack;「software-version」在日誌檔中缺少

### 2.3.0

*（發行日期：2016年9月15日）*

**補充：**

* &amp;lbrack;Plugin&amp;rbrack;新的「匯出到 Photoshop」插件（匯出完整圖層堆疊）
* &amp;lbrack;Export&amp;rbrack;允許指定填充的寬度（像素或無限）
* &amp;lbrack;Export&amp;rbrack; 允許設定 UV 外的背景類型
* &amp;lbrack;Shelf&amp;rbrack;新的材質分層著色器，可以混合 10 種材質
* &amp;lbrack;Shelf&amp;rbrack;新的黏土著色器，可透過高度/法線通道查看細節
* &amp;lbrack;Shelf&amp;rbrack;新的烘焙光影濾鏡，帶有環境輸入
* &amp;lbrack;Shelf&amp;rbrack;更新了一些遮罩產生器，加入了非平方變換
* &amp;lbrack;Viewport&amp;rbrack; 在 Solo 模式中新增合成法線貼圖（法線+高度+烘焙）
* &amp;lbrack;腳本&amp;rbrack; 允許匯出更多地圖
* &amp;lbrack;Scripting&amp;rbrack; 允許查詢可用 每個材質集的額外貼圖
* &amp;lbrack;腳本&amp;rbrack; 允許擷取頻道格式
* &amp;lbrack;腳本&amp;rbrack;在烘焙文件中加入範例
* &amp;lbrack;Scripting&amp;rbrack; 允許查詢圖層的可見性
* &amp;lbrack;Scripting&amp;rbrack; 允許查詢圖層的混合模式與不透明度
* &amp;lbrack;腳本&amp;rbrack;允許匯出轉換後的地圖（最終法線貼圖、混合 AO 等）
* &amp;lbrack;Substance&amp;rbrack;閱讀並連結自訂用法
* &amp;lbrack;Shortcuts&amp;rbrack; 新增修飾鍵（SHIFT）可逆向單人模式
* &amp;lbrack;Export&amp;rbrack;已更新預設匯出預設，禁用 alpha
* &amp;lbrack;UI&amp;rbrack;縮圖現在只有在引擎可用時才會計算
* &amp;lbrack;UI&amp;rbrack;當縮圖正在計算時，請顯示提及

**修正：**

* 打開舊專案時會當機
* 當機時材質通道快取損壞
* 使用 Material Layering 工作流程混合超過 4 種材質時會當機
* &amp;lbrack;UI&amp;rbrack;工具快捷鍵如果隱藏了就無法使用。
* &amp;lbrack;UI&amp;rbrack;Iray 工具列在檢視選單中標示為「Untitled」
* &amp;lbrack;UI&amp;rbrack;插件工具列在檢視選單中命名為「Untilted」
* &amp;lbrack;Baker&amp;rbrack;在編輯烘焙設定時按下 Enter 會啟動烘焙過程
* &amp;lbrack;Baker&amp;rbrack;某些參數的範圍錯誤
* &amp;lbrack;Import&amp;rbrack;因為數字太大，無法匯入 OBJ 網格
* &amp;lbrack;Import&amp;rbrack;有些 OBJ 檔案匯入時子物件太多
* &amp;lbrack;Export&amp;rbrack;通道背景在輸出時以黑色填滿，而非預設顏色
* &amp;lbrack;工具&amp;rbrack;粒子如果視野太低就無法正常運作
* &amp;lbrack;Tool&amp;rbrack;子堆疊中的遮罩時，筆刷預覽顏色不正確
* &amp;lbrack;視窗&amp;rbrack;當刷子進入2D視圖中的空曠區域時，會變得巨大無比
* &amp;lbrack;Viewport&amp;rbrack;繪製法線貼圖時的空白筆刷預覽
* &amp;lbrack;Scripting&amp;rbrack;文件錯誤：標示「ao」而非「ambientocclusion」
* &amp;lbrack;Scripting&amp;rbrack; 以 subprocess（） 啟動的程序在關閉 Painter 時會被終止
* &amp;lbrack;Shelf&amp;rbrack;烘焙燈光濾鏡使用錯誤的AO輸入
* &amp;lbrack;MacOS&amp;rbrack;移除消防栓專案（不相容）
* 預設專案在載入 \*.spt 檔案時會開啟（而非 \*.spp）。

**已知問題：**

* &amp;lbrack;Plugin&amp;rbrack;因為 Photoshop，高度和法線通道無法直接翻譯

### 2.2.0

*（發行日期：2016年7月22日）*

**補充：**

* &amp;lbrack;Shelf&amp;rbrack;改進搜尋系統與查詢
* &amp;lbrack;Shelf&amp;rbrack;新增迷你書架搜尋欄位
* &amp;lbrack;著色器&amp;rbrack;允許定義滑桿的階躍精度
* &amp;lbrack;Shader&amp;rbrack; 新增一個復原/重做按鈕用於著色器參數
* &amp;lbrack;Shader&amp;rbrack;重新載入著色器不應該重置其參數
* &amp;lbrack;MatLayering&amp;rbrack;新增對動態材質分層及子堆疊的支援
* &amp;lbrack;MatLayering&amp;rbrack; 允許匯入 json 檔案以設定著色器設定
* &amp;lbrack;MatLayering&amp;rbrack; 解鎖材質取樣器的限制（切換為無綁定材質）
* &amp;lbrack;腳本&amp;rbrack;允許設定烘焙者設定並啟動計算
* &amp;lbrack;Substance&amp;rbrack;除了識別碼外，還要用「usage」表示輸入/輸出連接
* &amp;lbrack;Tool&amp;rbrack; 允許在投影工具的視窗中選擇預覽通道

**修正：**

* 如果藥物放在錯誤資料夾裡，啟動時會當機
* 當機報告有時因為日誌檔案錯誤而無法運作
* &amp;lbrack;Iray&amp;rbrack;當 Iray 暫停時，後期效果不會刷新
* &amp;lbrack;Iray&amp;rbrack;自動對焦快捷鍵不再有效了
* &amp;lbrack;Iray&amp;rbrack;光圈滑桿行為會根據資產大小改變
* &amp;lbrack;Layers&amp;rbrack;如果所有素材通道都被關閉，預設不會啟用
* &amp;lbrack;Shader&amp;rbrack;若「param auto」錯誤，則不會列印錯誤

**已知問題：**

* &amp;lbrack;Mac&amp;rbrack;材質取樣限制鎖定在 16（GPU 驅動程式問題）

### 2.1.1

*（發行日期：2016年7月1日）*

**補充：**

* &amp;lbrack;License&amp;rbrack;能夠更改授權檔案的位置
* &amp;lbrack;Viewport&amp;rbrack; 新增一個「B」捷徑以在其他地圖間循環使用
* &amp;lbrack;Import&amp;rbrack;允許正確匯入 FBX 2016/2017
* &amp;lbrack;工具&amp;rbrack;使用快速遮罩時移除棋盤
* &amp;lbrack;Iray&amp;rbrack; 新增場景尺寸資訊
* &amp;lbrack;Iray&amp;rbrack;允許增加最大取樣數與渲染時間
* &amp;lbrack;UI&amp;rbrack;使用滑桿上的 +/- 按鈕時立即更新結果
* &amp;lbrack;UI&amp;rbrack;允許灰階滑桿更精確
* &amp;lbrack;Export&amp;rbrack;不要匯出只支援 RGB 材質的 alpha 通道
* &amp;lbrack;Export&amp;rbrack; Update Dota 2 export preset
* &amp;lbrack;Shelf&amp;rbrack;新「六角形瓷磚」圖案
* &amp;lbrack;架子&amp;rbrack;新「焊接」工具
* &amp;lbrack;Shelf&amp;rbrack;更新後面濾鏡以提供方向控制

**修正：**

* &amp;lbrack;Export&amp;rbrack;無法以 8 位元匯出 PSD 檔案
* &amp;lbrack;Export&amp;rbrack;部分硬體配置無法提供 8K 匯出
* &amp;lbrack;Export&amp;rbrack;Sketchfab 視窗被裁切
* &amp;lbrack;Export&amp;rbrack;Spec/Gloss 匯出預設中粗糙度貼圖錯誤
* &amp;lbrack;UI&amp;rbrack; 打灰階滑桿已經不行了
* &amp;lbrack;UI&amp;rbrack;無法將過濾器放入物質輸入（像是產生器）
* &amp;lbrack;UI&amp;rbrack;有些滑桿有奇怪的行為
* &amp;lbrack;UI&amp;rbrack; DeltaTime +/- 粒子的步長太大了
* &amp;lbrack;Iray&amp;rbrack;有些專案在切換到 Iray 時會阻擋該應用程式
* &amp;lbrack;Iray&amp;rbrack;偵測硬體時的崩潰
* &amp;lbrack;Tool&amp;rbrack;遮罩模式下筆刷預覽顏色不正確
* &amp;lbrack;工具&amp;rbrack;材料選擇器可用於不相容的工具
* &amp;lbrack;Tool&amp;rbrack;投影預覽不會切換到帶有 Spec/Gloss 的漫遊工作流程
* &amp;lbrack;Shelf&amp;rbrack;更改預設著色器會破壞智慧墊/智慧遮罩預覽
* &amp;lbrack;Shelf&amp;rbrack;有些智慧材料名稱有誤
* &amp;lbrack;Shelf&amp;rbrack;額外的 alpha 形狀被損壞，無法載入
* &amp;lbrack;Viewport&amp;rbrack;切換到「附加地圖」模式時，先顯示「其他」
* &amp;lbrack;Viewport&amp;rbrack;當沒有額外地圖時，視窗切換回「其他」
* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Linux&amp;rbrack;崩潰報告在 Ubuntu（Steam）上無法運作
* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Linux&amp;rbrack; Web URL links 在 Ubuntu （Steam） 上無法使用
* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Windows&amp;rbrack; 當 Substance 畫家不再執行時，移除「crashwatcher」
* &amp;lbrack;Crash&amp;rbrack;&amp;lbrack;Mac&amp;rbrack;崩潰報告系統無法正常運作
* &amp;lbrack;Crash&amp;rbrack; 匯入網格同時已經匯入網格會導致崩潰
* 材質集選擇捷徑在重新啟動後會重置成無

### 2.1.0

*（發行日期：2016年6月2日）*

**補充：**

* &amp;lbrack;UDIM&amp;rbrack; 從網格匯入 UDIM 磚塊作為貼圖集
* &amp;lbrack;Linux&amp;rbrack;新增對 CentOS 6.6 與 Ubuntu 12.4 的支援
* &amp;lbrack;Export&amp;rbrack; 新增 8K 解析度（實驗性）
* &amp;lbrack;Export&amp;rbrack;允許在匯出時選擇位深
* &amp;lbrack;Baker&amp;rbrack;允許同時烘焙多個貼圖集
* 支援高解析度螢幕（高 DPI 縮放）
* &amp;lbrack;Scripting&amp;rbrack; 在匯出時設定每個材質的自訂解析度與填充
* &amp;lbrack;Viewport&amp;rbrack; 允許透過點擊網格（透過 Ctrl+Alt+Click）切換材質集
* &amp;lbrack;Viewport&amp;rbrack;用滑鼠滾輪縮放時，移動滑鼠游標所在的位置
* &amp;lbrack;UI&amp;rbrack; 更新預設背景色與環境地圖顯示
* &amp;lbrack;UI&amp;rbrack;新增使用者頻道的原始名稱工具提示
* &amp;lbrack;UI&amp;rbrack; 更改無法重命名頻道的背景色
* &amp;lbrack;工具&amp;rbrack;使用快速遮罩時移除棋盤
* &amp;lbrack;Shader&amp;rbrack;允許定義著色器參數與材質/遮罩的群組
* &amp;lbrack;Engine&amp;rbrack;小型沖壓的優化
* &amp;lbrack;模板&amp;rbrack;將「W」作為快捷鍵，暫時切換遮罩
* &amp;lbrack;Shelf&amp;rbrack; 新增一個十字鍵以清除搜尋欄
* &amp;lbrack;Shelf&amp;rbrack;一鍵載入 Alpha
* &amp;lbrack;Shelf&amp;rbrack;新匯出預設：Vray UDIM、Arnold UDIM、Spec/Gloss（來自 Metal/Rough）
* &amp;lbrack;Shelf&amp;rbrack;新alpha：幾何形狀、脈絡與符號
* 在 Substance Painter 執行檔的屬性中新增名稱和版本

**修正：**

* &amp;lbrack;Substance&amp;rbrack;無法同時使用正常通道與額外地圖
* &amp;lbrack;Iray&amp;rbrack;MDL 折射與吸收設定無法運作
* &amp;lbrack;Iray&amp;rbrack;原始場景比例未被保存
* &amp;lbrack;Shelf&amp;rbrack;鏡面/光澤模板使用錯誤著色器
* &amp;lbrack;Export&amp;rbrack;預設匯出預設不會匯出某些地圖（像是 AO）
* &amp;lbrack;Viewport&amp;rbrack; 在 2D 視圖中點擊 UV 外時，樞軸點不會更新
* &amp;lbrack;UI&amp;rbrack;滑桿值為四捨五入
* &amp;lbrack;UI&amp;rbrack;有時編輯滑桿值時，空閒空間非常小
* &amp;lbrack;新專案&amp;rbrack;範本下拉選單未正確更新（從 1.x 更新到 2.x）
* &amp;lbrack;腳本&amp;rbrack; 修正自訂按鈕的「懸停」行為
* &amp;lbrack;Mac&amp;rbrack;取消空專案會鎖定攝影機

**已知問題：**

* Ubuntu 上無法提供當機報告
* 有些網址按鈕可能無法使用，請參考我們的常見問題解答

### 2.0.5

*（發行日期：2016年4月29日）*

**補充：**

* &amp;lbrack;Shelf&amp;rbrack;新增/更新非 PBR 模板、著色器及匯出預設
* &amp;lbrack;Shelf&amp;rbrack;更新 UE4 匯出預設，加入環境遮蔽

**修正：**

* 開啟並儲存某些資源損壞的專案時會當機
* &amp;lbrack;視窗&amp;rbrack;線框在2D視圖中看起來斷裂
* &amp;lbrack;Shelf&amp;rbrack;提升部分工作室環境地圖的效能
* &amp;lbrack;Shelf&amp;rbrack;部分工作室環境地圖會被複製
* &amp;lbrack;Shelf&amp;rbrack;缺少「烘焙燈光材料」
* &amp;lbrack;Shelf&amp;rbrack;缺少「灰階轉換」產生器

### 2.0.4

*（發行日期：2016年4月26日）*

**補充：**

* 改善網格碰撞並優化線框渲染
* 透過大型專案提升效能與記憶體管理
* 提升滑桿精準度與步進感
* &amp;lbrack;UI&amp;rbrack;僅在驗證滑桿時更新引擎（不在輸入值時）
* &amp;lbrack;UI&amp;rbrack;將 Iray 開關移到主工具列的專用按鈕（並更改快捷鍵）
* &amp;lbrack;Tool&amp;rbrack; 新增克隆工具來源位置行為設定
* &amp;lbrack;Shader&amp;rbrack;允許在自訂著色器中讀取網格頂點顏色
* &amp;lbrack;腳本&amp;rbrack;允許檢索紋理集、通道與圖層的列表
* &amp;lbrack;Scripting&amp;rbrack;新增輔助功能（網址到路徑，取得專案匯出路徑）
* &amp;lbrack;Mac&amp;rbrack; 在日誌檔中偵測 Mac OS 「El Capitan」版本

**修正：**

* 第二次出口到 Substance Share 後崩盤
* 在使用 Quick Mask 資料複製圖層時會當機。
* 有些專案的更新器非常長，會消耗大量記憶體
* &amp;lbrack;Tool&amp;rbrack;使用 clone/smudge tool 選擇粒子預設時會當機
* &amp;lbrack;Baker&amp;rbrack;載入 FBX 檔案對於重網格來說太花時間了
* &amp;lbrack;Viewport&amp;rbrack;部分電腦上的拉伸環境地圖
* &amp;lbrack;視窗&amp;rbrack;畫筆α轉換錯誤的伽瑪
* &amp;lbrack;Export&amp;rbrack;Alpha 會以透明檔儲存，而不是用 Tiff 檔案獨立的通道。
* &amp;lbrack;Export&amp;rbrack;一般通道總是匯出為 OpenGL
* &amp;lbrack;Iray&amp;rbrack;缺少 Iray 設定的滑桿名稱
* &amp;lbrack;Iray&amp;rbrack;渲染在 Retina/High DPI 上解析度錯誤
* &amp;lbrack;Iray&amp;rbrack;在 Iray 模式下調整介面大小時會當機
* &amp;lbrack;Iray &amp;rbrack;在某些低解析度下渲染時，效能大幅下降
* &amp;lbrack;Iray&amp;rbrack;暫停不行（Iray 仍在背景計算）
* 正常通道有時會出現黑色方形的偽影
* 法線通道由灰階濾波器反轉
* 如果堆疊中有一些 alpha，普通通道就無法好好融合
* 即使專案還沒儲存，打開專案時也會在磁碟上編輯
* 在某些專案中重新匯入網格會讓 GPU 效能非常差
* 當不接觸網格時，筆刷方向是錯誤的
* 歡迎畫面中缺少 Substance Share 標誌

### 2.0.2

*（發行日期：2016年3月25日）*

**補充：**

* &amp;lbrack;Iray&amp;rbrack;更新規格/光澤模板與著色器以相容 Iray
* &amp;lbrack;匯出&amp;rbrack;能夠將截圖匯出到 ArtStation
* &amp;lbrack;Scripting&amp;rbrack; 支援從插件目錄執行
* &amp;lbrack;Scripting&amp;rbrack; 允許「另存為」
* &amp;lbrack;UI&amp;rbrack; 允許雙擊滑桿以編輯其值
* 將 Vela 樣本移至 Substance 分享
* 全新範例專案：Sphere 預覽
* 提醒使用者 shell 擴充功能衝突

**修正：**

* Substance Painter 1.x 安裝程式覆蓋安裝
* &amp;lbrack;UI&amp;rbrack;頻道列表配置因過濾器而失效
* &amp;lbrack;UI&amp;rbrack;著色器參數不會顯示
* &amp;lbrack;UI&amp;rbrack;調整圖層視窗大小會錯誤裁切內容
* &amp;lbrack;工具&amp;rbrack;不透明度通道並不總是被正確使用
* &amp;lbrack;Tool&amp;rbrack;Smudge/Clone 無法與對稱性相符
* &amp;lbrack;Tool&amp;rbrack;部分通道的筆刷預覽透明度不正確
* &amp;lbrack;Iray&amp;rbrack;在尚未建立 Iray 時會當機
* &amp;lbrack;Iray&amp;rbrack; 無法從專案載入 iray 設定資料
* &amp;lbrack;Iray&amp;rbrack;Iray 暫停後不會處理設定修改
* &amp;lbrack;Shelf&amp;rbrack;將材料匯入貨架無法運作
* 模板無法在 Normal 通道上使用
* 在某些專案上繪畫時會當機
* 在某些專案中用粒子上色時會當機
* 在某些運算過程中，Pixel 處理器會當機

### 2.0.0

*（發行日期：2016年3月16日）*

**補充：**

* 主工具列中 Substance Store 的捷徑
* Iray 渲染器，具備檢視模式和截圖匯出功能
* 支援「智慧口罩」的創建與使用
* 支援 Specular/Glossines PBR 工作流程（新增擴散通道）
* 鏈化物質（將物質插入物質影像輸入）
* 以自訂外掛支援腳本
* 透過使用 Sobel 濾波器提升高度轉換為法線的轉換
* 將模板/投影預覽解析度切換為 2K
* 新專案預設新增一般頻道
* 從輸出節點讀取使用者資料標籤，預設即可啟用或停用某物質的通道
* 在 TextureSet 設定中露出法線/AO 混合
* &amp;lbrack;工具&amp;rbrack;用於混合與擴散色彩的新暈染工具
* &amp;lbrack;Tool&amp;rbrack;新複製工具，用於複製部分貼圖
* &amp;lbrack;工具&amp;rbrack;允許選擇污漬、克隆及橡皮擦工具的通道
* &amp;lbrack;Layer&amp;rbrack; 為填充效果名稱新增物質名稱
* &amp;lbrack;Layer&amp;rbrack; 允許將遮罩匯出到剪貼簿
* &amp;lbrack;視窗&amp;rbrack;切換透視與正字模式
* &amp;lbrack;Viewport&amp;rbrack; 允許在透視模式下控制視野
* &amp;lbrack;Viewport&amp;rbrack;允許以 CTRL+Middle Click 設定景深距離
* &amp;lbrack;Viewport&amp;rbrack;允許在 3D 視圖中拖放環境地圖。
* &amp;lbrack;視窗&amp;rbrack;當引擎進行強運算時，回饋效果會更好
* &amp;lbrack;Export&amp;rbrack; 允許將著色器參數匯出成 json 檔案
* &amp;lbrack;UI&amp;rbrack;更新介面，新增圖示、顏色與版面配置
* &amp;lbrack;UI&amp;rbrack;將資產名稱加入迷你書架
* &amp;lbrack;UI&amp;rbrack; 預設為「通道映射」
* &amp;lbrack;著色器&amp;rbrack;為著色器材質參數選擇自訂顏色
* &amp;lbrack;Shelf&amp;rbrack;拖放資源時詢問檔案要匯入哪裡
* &amp;lbrack;Shelf&amp;rbrack;智慧材料與發電機新預覽球體
* &amp;lbrack;Shelf&amp;rbrack;新增鏡面光澤著色器
* &amp;lbrack;Shelf&amp;rbrack;新硬質表面形狀
* &amp;lbrack;Shelf&amp;rbrack;新 Alpha 材質與形狀
* &amp;lbrack;Shelf&amp;rbrack;新皮膚材質
* &amp;lbrack;Shelf&amp;rbrack;基於新掃描的材料與智慧材料
* &amp;lbrack;Shelf&amp;rbrack;新的智慧材料與舊材質的規格/光澤支援
* &amp;lbrack;Shelf&amp;rbrack;用於金屬表面模擬的新製光處理過濾器
* &amp;lbrack;Shelf&amp;rbrack;全新強大的遮罩產生器「遮罩編輯器」
* &amp;lbrack;Shelf&amp;rbrack;重新加工並清洗舊材料
* 全新「Vela」樣本專案

**修正：**

* &amp;lbrack;設定&amp;rbrack;攝影機旋轉與縮放速度會被專案覆蓋
* &amp;lbrack;Viewport&amp;rbrack;預設法線貼圖的精度問題會導致反射錯誤
* &amp;lbrack;Viewport&amp;rbrack;Vignette 預設已啟用
* &amp;lbrack;Viewport&amp;rbrack;雜訊會出現在環境地圖邊界（Nvidia GPU）
* &amp;lbrack;Viewport&amp;rbrack;投影/模板模式下的縮圖載入時間非常長
* &amp;lbrack;Baker&amp;rbrack;將烘焙的材質儲存為 16 位元整數，而非 32 位元
* &amp;lbrack;Layer&amp;rbrack;過時物質在堆疊中顯示錯誤
* 某些通道的預設顏色和位元深度不正確（例如：鏡面、光澤）
* 修正橡皮擦行為以在直通模式下關閉混合

**已知問題：**

* 對稱性在 Smudge 和 Clone 工具上不適用
* ArtStation 匯出遺失

## 版本 1

### 1.7.3

*（發行日期：2016年3月1日）*

**補充：**

* &amp;lbrack;Export&amp;rbrack; 新增一個關閉填充的選項
* &amp;lbrack;Shelf&amp;rbrack;在架式資料夾中支援子層級結構

**修正：**

* 在之前只讀檔案上存檔時會當機
* 開啟第二個專案時當機
* 載入某些縮圖（書架、圖層或工具提示）時會當機
* 關閉「保留網格上的筆劃位置」無法運作
* &amp;lbrack;Export&amp;rbrack;點陣圖的放大是透過最近篩選完成的
* &amp;lbrack;Shelf&amp;rbrack;資源的發現非常緩慢
* &amp;lbrack;Shelf&amp;rbrack;模糊濾波器不支援 16 位元
* &amp;lbrack;Tool&amp;rbrack;如果你載入舊工具預設，對稱性就無法運作
* Specular 通道的色彩對話不會做色彩空間轉換

### 1.7.2

*（發行日期：2016年1月13日）*

**補充：**

* &amp;lbrack;Layers&amp;rbrack; 允許指定填充層的預設耕作

**修正：**

* &amp;lbrack;Export&amp;rbrack;Sketchfab 匯出功能不再運作
* &amp;lbrack;Layer&amp;rbrack;即使在填充時，也會進行雙線性濾波，無需任何轉換
* &amp;lbrack;工具&amp;rbrack;在投影模式下使用帶有影像輸入的物質表現不佳
* &amp;lbrack;工具&amp;rbrack;材料選擇器壞了

### 1.7.1

*（發行日期：2015年12月18日）*

**修正：**

* 切換材質集時會當機
* 繪畫時的緩慢表現

### 1.7.0

*（發行日期：2015年12月17日）*

**補充：**

* &amp;lbrack;Performances&amp;rbrack;同時計算圖層內容及其縮圖
* &amp;lbrack;Export&amp;rbrack; 將匯出路徑儲存為相對於專案時的狀態
* &amp;lbrack;Layers&amp;rbrack;新增混合模式：減法與加/加
* &amp;lbrack;Layers&amp;rbrack;新的雙線性 HQ 填充層過濾
* &amp;lbrack;Shader&amp;rbrack;在偏好設定中設定預設的縮圖產生著色器。
* &amp;lbrack;Shader&amp;rbrack;允許為每個貼圖集指定一個著色器
* &amp;lbrack;Shader&amp;rbrack;允許從架子取樣貼圖
* &amp;lbrack;Tool&amp;rbrack;新的「包裹」筆刷行為用於繪畫
* &amp;lbrack;工具與工具;改良濾波並減少上色時的鋸齒
* &amp;lbrack;工具&amp;rbrack;提升子像素繪製品質
* &amp;lbrack;工具&amp;rbrack;移除了筆刷設定的「基本」顯示，並改善了框架開啟/關閉圖示
* &amp;lbrack;Menu&amp;rbrack;在右鍵選單中新增效果圖示
* 從專案中建立範本
* &amp;lbrack;Shelf&amp;rbrack;新模板：PBR、Dota 2
* &amp;lbrack;Shelf&amp;rbrack;新匯出預設：Dota 2
* &amp;lbrack;Shelf&amp;rbrack;新著色器：Dota 2、PBR 車漆、PBR 塗層、PBR 天鵝絨
* &amp;lbrack;架子&amp;rbrack;新材料：鋼鐵鏽蝕與磨損，風格化燈光
* &amp;lbrack;Shelf&amp;rbrack;新濾鏡：模糊定向、風格化光影
* &amp;lbrack;Shelf&amp;rbrack;新刷子：預設軟刷和預設硬刷，並用新的 alpha 法以提升硬度控制
* &amp;lbrack;Shelf&amp;rbrack;新產生器：3D 距離與光線
* &amp;lbrack;Shelf&amp;rbrack;更新筆刷，具備包覆投影與背面剔除功能（預設啟用）
* &amp;lbrack;Shelf&amp;rbrack;更新白噪音並搭配像素處理器版本，以加快計算速度

**修正：**

* &amp;lbrack;歡迎畫面&amp;rbrack;教學連結 傳送至舊影片
* &amp;lbrack;Channels&amp;rbrack; 說「no」以填入 AO 的圖層創建，仍會建立該圖層
* &amp;lbrack;Channels&amp;rbrack;UserX 通道名稱不會在介面中傳播
* &amp;lbrack;Viewport&amp;rbrack;掩罩條目在個人頻道列表中是空的
* &amp;lbrack;Share&amp;rbrack;從 SP 匯出 alpha 到 Share，會產生無法讀取的 .image 檔案
* &amp;lbrack;License&amp;rbrack; 修正非 ASCII 字元使用者名稱啟用問題
* &amp;lbrack;Shader&amp;rbrack;選取顏色時，顏色參數對話會消失
* &amp;lbrack;Shelf&amp;rbrack;未使用時縮圖不會從記憶體中卸載
* &amp;lbrack;Shelf&amp;rbrack;固定梯度濾波器
* &amp;lbrack;Tool&amp;rbrack;對稱性不適用於模板/投影
* &amp;lbrack;Tool&amp;rbrack;建立新筆刷預設時名稱錯誤
* 即使重新匯入網格，保留筆劃設定仍是關閉狀態
* 當計算粒子大小很大時，驅動子重置（TDR）。

### 1.6.1

*（發行日期：2015年11月9日）*

**修正：**

* 如果 2D 視圖顯示，開啟專案時會當機
* 如果目前的書架不存在，建立新的匯出預設時會當機
* &amp;lbrack;工具&amp;rbrack;材料選擇器圖示可以持續顯示
* &amp;lbrack;Tool&amp;rbrack;材質選擇器在同時繪製時會隱藏滑鼠游標
* &amp;lbrack;Shelf&amp;rbrack;每次退出後，中繼資料都會寫入磁碟

### 1.6.0

*（發行日期：2015年10月29日）*

**補充：**

* Windows 10 官方支援
* &amp;lbrack;Substance&amp;rbrack;預設收斂物質參數群組
* &amp;lbrack;Substance&amp;rbrack; 新增框架（提升像素處理器效能）
* &amp;lbrack;視窗&amp;rbrack;允許在對稱模式下停用對稱平面顯示。
* &amp;lbrack;Viewport&amp;rbrack;改善陰影渲染與效能
* &amp;lbrack;視窗&amp;rbrack;繪畫時暫停陰影計算
* &amp;lbrack;Viewport&amp;rbrack; 提升線框渲染效能
* &amp;lbrack;引擎&amp;rbrack;改進 VRAM 記憶體管理以減少其佔用
* &amp;lbrack;Engine&amp;rbrack;提升 AMD GPU 的材質刷新以提升效能
* &amp;lbrack;Engine&amp;rbrack;為了提升效能，請關閉 NVIDIA GPU 的執行緒優化設定
* &amp;lbrack;Effect&amp;rbrack; 新增標籤以請求「填充」影像輸入
* &amp;lbrack;Layer&amp;rbrack;提升填充中紫外線偏移/比例的精度
* &amp;lbrack;Layer&amp;rbrack;在填充時讓比例滑桿呈指數型
* &amp;lbrack;Layer&amp;rbrack;允許直接拖放材料到圖層堆疊中。
* &amp;lbrack;Layer&amp;rbrack; 允許直接拖放濾波器在圖層堆疊中
* &amp;lbrack;Layer&amp;rbrack; 調整遮罩刷子顏色到新建立的遮罩顏色
* &amp;lbrack;Shader&amp;rbrack;暴露多個 texcoords
* &amp;lbrack;Shader&amp;rbrack;公開 gamma/tonemapping 函式以允許自訂功能
* &amp;lbrack;Bakers&amp;rbrack; 更改預設位置 Baker 設定以用於 TriPlanar 使用。
* &amp;lbrack;工具&amp;rbrack;將「幾何貼紙」重新命名為「多邊形填充」
* &amp;lbrack;Shelf&amp;rbrack;更新產生器以支援三平面：MG 金屬邊緣磨損、MG 面罩組裝器、MG 玻璃纖維、MG Dirt
* &amp;lbrack;Shelf&amp;rbrack;更新材料，新增設定並移除未使用的材料
* &amp;lbrack;Shelf&amp;rbrack;22 種新型智慧材料（塑膠、鐵、布料、鋼材等）
* &amp;lbrack;Shelf&amp;rbrack;更新銳化、模糊與變形濾鏡，並加入填充影像輸入以避免接縫
* &amp;lbrack;Shelf&amp;rbrack;改善Warp設定以便使用。
* &amp;lbrack;Shelf&amp;rbrack;2 新程序噪音：3D Perlin 噪音與 3D Worley 噪音

**修正：**

* &amp;lbrack;Engine&amp;rbrack;Mac 上專用 GPU 的 VRAM 數量偵測不正確
* &amp;lbrack;Engine&amp;rbrack;在視窗中，貼圖會轉為較暗的版本
* &amp;lbrack;Engine&amp;rbrack;在多層下方塗裝時表現不佳
* &amp;lbrack;Engine&amp;rbrack;開啟專案時計算的層與快取版本不同
* &amp;lbrack;Substance&amp;rbrack;Mac 上 4K 的錯誤結果
* &amp;lbrack;Substance&amp;rbrack;參數順序錯誤
* &amp;lbrack;著色器&amp;rbrack;Toon 和 Pixelated 著色器都是完全黑色的
* &amp;lbrack;Shader&amp;rbrack;參數在更換環境映射後消失
* &amp;lbrack;Shelf&amp;rbrack;將 png 檔案放入產生器資料夾時會當機
* &amp;lbrack;Shelf&amp;rbrack;縮圖以低粗糙度產生
* &amp;lbrack;Tool&amp;rbrack;在 Windows 筆刷 alpha 中使用點陣圖時會當機
* &amp;lbrack;Export&amp;rbrack; 額外的地圖匯出預設現在匯出一個 RGB 地圖作為位置

### 1.5.7

*（發行日期：2015年9月24日）*

**修正：**

* 崩潰報告不再有效

### 1.5.6

*（發行日期：2015年9月21日）*

**補充：**

* &amp;lbrack;Shelf&amp;rbrack;提升縮圖渲染品質（使用 1K 材質）

**修正：**

* &amp;lbrack;分享&amp;rbrack;無法用其他帳號簽名
* &amp;lbrack;Shelf&amp;rbrack;縮圖在磁碟上太重了
* &amp;lbrack;Shelf&amp;rbrack;智慧材料載入速度非常慢
* &amp;lbrack;Windows&amp;rbrack; 修正授權服務安裝
* &amp;lbrack;Channels&amp;rbrack;預設為 G8 建立傳輸映射

### 1.5.5

*（發行日期：2015年9月15日）*

**補充：**

* &amp;lbrack;Shelf&amp;rbrack;資產出口至Substance Share。
* &amp;lbrack;Shelf&amp;rbrack; 新增材料球預覽
* &amp;lbrack;Shelf&amp;rbrack;使用環境貼圖「Glazed Patio」來產生縮圖
* &amp;lbrack;Shelf&amp;rbrack;將縮圖解析度提升至 512x512 像素
* &amp;lbrack;3D 檢視&amp;rbrack; 顯示環境旋轉值
* &amp;lbrack;Windows&amp;rbrack;簽署應用程式

**修正：**

* &amp;lbrack;Bakers&amp;rbrack;同時烘焙地圖時會出現錯誤結果
* &amp;lbrack;3D 檢視&amp;rbrack;當沒有專案開啟時，環境圖會顯示
* &amp;lbrack;Layers&amp;rbrack;遮罩產生器無法處理圖層內容
* &amp;lbrack;Layers&amp;rbrack;你可以在隱藏圖層上繪畫
* &amp;lbrack;Shelf&amp;rbrack;Dirt_5和Dirt_6噪音是一樣的
* &amp;lbrack;Shelf&amp;rbrack;有些遮罩產生器會被像素化或品質低
* &amp;lbrack;工具&amp;rbrack;某些角度的裝置旋轉錯誤。
* &amp;lbrack;工具&amp;rbrack;通道過多會導致通道按鈕被裁切掉
* &amp;lbrack;工具&amp;rbrack;快速遮罩的反轉遮罩捷徑無法使用
* &amp;lbrack;Export&amp;rbrack; Sketchfab：取消按鈕未正確考慮
* &amp;lbrack;License&amp;rbrack;當無法複製授權時啟動失敗
* 幀率限制器在介面上已經無法使用

### 1.5.0

*（發行日期：2015年8月20日）*

**補充：**

* &amp;lbrack;Shader&amp;rbrack;在 Shader 編譯錯誤訊息中加入行號
* &amp;lbrack;Shelf&amp;rbrack;提升縮圖預覽品質
* &amp;lbrack;Shelf&amp;rbrack;智慧材料的縮圖自動生成
* &amp;lbrack;工具&amp;rbrack;控制物質硬度設定的捷徑
* &amp;lbrack;Tool&amp;rbrack;在遮罩上使用灰階小工具來貼幾何貼紙
* &amp;lbrack;工具&amp;rbrack;在灰階地圖上繪畫時反推顏料顏色的捷徑
* &amp;lbrack;Viewport&amp;rbrack; 允許顯示線框並改變其顏色
* &amp;lbrack;視窗&amp;rbrack;模糊環境背景
* &amp;lbrack;Controls&amp;rbrack; 為刷滑鼠滑鼠切換加入旋轉功能
* &amp;lbrack;Export&amp;rbrack;匯出至 Sketchfab
* &amp;lbrack;Export&amp;rbrack; 建立渲染器的匯出預設
* &amp;lbrack;Export&amp;rbrack; 新增轉換後的地圖反射、F0 和 1/IOR
* &amp;lbrack;UI&amp;rbrack; 新增歡迎畫面
* &amp;lbrack;UI&amp;rbrack; 更新預設版面
* &amp;lbrack;UI&amp;rbrack;新增缺少的工具提示並重新命名部分選單條目
* &amp;lbrack;Layers&amp;rbrack; 匯出目前選取的遮罩為點陣圖
* &amp;lbrack;Layers&amp;rbrack;在右鍵選單中新增「反轉遮罩」動作

**修正：**

* &amp;lbrack;Project&amp;rbrack;如果 FBX 的網格樞軸不同，匯入時網格會被炸毀
* &amp;lbrack;物質&amp;rbrack;投影工具所用物質被鎖定在256\*256
* &amp;lbrack;Layers&amp;rbrack;使用透明遮罩時會崩潰
* &amp;lbrack;Export&amp;rbrack;非常暗材質上的伽瑪轉換錯誤
* &amp;lbrack;Export&amp;rbrack;位置貼圖只能在匯出預設中作為灰階貼圖使用。
* &amp;lbrack;工具&amp;rbrack;幾何貼紙起始顏色在遮罩上時為黑色
* &amp;lbrack;Tool&amp;rbrack;如果 alpha 沒有硬度，旋轉快捷鍵就無法使用。

### 1.4.2

*（發行日期：2015年7月15日）*

**修正：**

* &amp;lbrack;工具&amp;rbrack;使用幾何貼紙搭配快速遮罩時會崩潰
* 將專案從 1.4.0 更新到 1.4.1 會佔用所有電腦記憶體
* 舊專案格式匯入錯誤
* 自訂書架解析整個階層，並在各處複製資產

### 1.4.1

*（發行日期：2015年6月23日）*

**補充：**

* &amp;lbrack;視窗&amp;rbrack;允許將面板並排對接
* &amp;lbrack;Effect&amp;rbrack;為關卡效果新增背景和尺子
* &amp;lbrack;Effect&amp;rbrack; 新增一個能在其他效果上方運作的繪畫效果

**修正：**

* &amp;lbrack;Shelf&amp;rbrack;若沒有專案開啟，縮圖產生就壞掉了
* &amp;lbrack;Shelf&amp;rbrack; 材質預設預覽無法產生
* &amp;lbrack;Shelf&amp;rbrack;材質預覽是在帶有反法線的網格上產生的
* &amp;lbrack;Shelf&amp;rbrack;縮圖總是因為雜湊函數錯誤而重新計算
* &amp;lbrack;Shelf&amp;rbrack;點擊物質材質不會連結其他地圖
* &amp;lbrack;工具&amp;rbrack;用材料挑選器取樣的值錯誤
* &amp;lbrack;Tool&amp;rbrack;色彩選擇器選擇視窗游標顏色
* &amp;lbrack;2D 視圖&amp;rbrack;幀率/效能非常低
* &amp;lbrack;Export&amp;rbrack;開啟匯出視窗時匯出預設太新，會當機。
* &amp;lbrack;Export&amp;rbrack;Height 通道轉為法線貼圖，但被轉換到錯誤的空間
* &amp;lbrack;Mac&amp;rbrack;Substance Effects 的 BaseColor 會顯示為線性
* &amp;lbrack;Mac&amp;rbrack;直線小工具在 Retina 上被錯誤繪製
* 即使啟用捷徑，直線仍可維持啟用。
* 旋轉環境貼圖後，直線 guizmo 會消失
* 物質產生的環境遮蔽輸出不會自動接入AO通道
* 修正 Windows 上使用者名稱中特殊字元的授權複製問題

### 1.4.0

*（發行日期：2015年6月10日）*

**補充：**

* &amp;lbrack;Export&amp;rbrack;在可用輸入映射列表中新增更多映射
* &amp;lbrack;Shelf&amp;rbrack;使用 sbsar 材料作為材料預設
* &amp;lbrack;Shelf&amp;rbrack;允許使用自訂函式庫路徑
* &amp;lbrack;Shelf&amp;rbrack;更改最小尺寸
* &amp;lbrack;Shelf&amp;rbrack;新內容：20 種全新智慧材料
* &amp;lbrack;Shelf&amp;rbrack;新內容：新程序物質（織布、網格）
* &amp;lbrack;Shelf&amp;rbrack;更新模糊濾鏡
* 用修飾鍵畫直線
* 新增環境遮蔽通道，並重新調整層堆疊中的 AO/Normal 行為
* 從 Substance 使用者資料中定義的影像輸入讀取預設顏色
* 允許從說明選單匯出日誌

**修正：**

* &amp;lbrack;Baker&amp;rbrack;&amp;lbrack;Mac&amp;rbrack;從 mesh baker 與 Normal 當機
* &amp;lbrack;Baker&amp;rbrack;如果籠子檔案中沒有 UV，則當機
* &amp;lbrack;Baker&amp;rbrack;以名稱匹配無法用於從 zBrush 匯出的 OBJ。
* &amp;lbrack;Baker&amp;rbrack;如果使用多個材質集和重疊的 UV，使用 cage 烘焙會覆蓋烘焙
* &amp;lbrack;Baker&amp;rbrack;特定 OBJ 檔案會導致黑色貼圖
* &amp;lbrack;Shelf&amp;rbrack;若設為唯讀，無法讀取資源
* &amp;lbrack;Shelf&amp;rbrack;資產檔案若已用於專案，則會以畫家方式撰寫。
* &amp;lbrack;Shelf&amp;rbrack;重新裝填物質也會更新該層
* &amp;lbrack;Export&amp;rbrack;Tiff 匯出 32 位元圖片，Photoshop 或遊戲引擎無法正確讀取
* &amp;lbrack;Export&amp;rbrack;預設通道預設總是匯出為 RGB。
* &amp;lbrack;Material&amp;rbrack; 漫反射通道覆蓋基底色映射與物質
* &amp;lbrack;3D 視圖&amp;rbrack;特定環境貼圖下散射光影錯誤
* &amp;lbrack;工具&amp;rbrack;無法將畫筆旋轉到特定角度
* 視窗在滑鼠滑鼠上輸入文字欄位時會被聚焦
* 預設值太新，對目前版本的書架來說當機
* 更換網格後當機
* 在裝填不同輸入數量的物質時會當機
* 從 Cinema4D 匯入的 FBX 網格，材質名稱錯誤

### 1.3.5

*（發行日期：2015年5月29日）*

**補充：**

* &amp;lbrack;License&amp;rbrack;當已有授權檔案時，啟動問題
* &amp;lbrack;Mac&amp;rbrack;載入特定 FBX 檔案時會當機
* &amp;lbrack;Mac&amp;rbrack;&amp;lbrack;3D View&amp;rbrack;整合 GPU 的錯誤反射
* &amp;lbrack;3D 視圖&amp;rbrack;快速遮罩字型壞掉了
* &amp;lbrack;3D 視圖&amp;rbrack;材質選擇器會讓視窗完全變黑
* 開啟 1.3.3 建立的專案後當機
* 使用 alpha 的著色器時，材質預覽是空的
* 塗裝會停止對特定網格進行
* 使用特定 OBJ 網格時，效能會大幅下降
* 使用效果時，使用者通道不會被映射
* 暫存資料夾在啟動時不會被清理

**修正：**

* 專案的計算時間提升非常長，載入時間非常長
* 把「GPU 故障排除」視窗改成更容易理解
* &amp;lbrack;Layers&amp;rbrack;儲存填充層的比率鎖定狀態，並預設為「開啟」
* &amp;lbrack;Bakers&amp;rbrack;現在以名字匹配時，使用後綴作為分隔符

### 1.3.4

*（發行日期：2015年4月27日）*

**補充：**

* &amp;lbrack;Mac&amp;rbrack;與 Mac OS X Yosemite（10.10） 一起崩潰
* &amp;lbrack;Mac&amp;rbrack;無法退出全螢幕模式
* &amp;lbrack;Bakers&amp;rbrack;以名字配對的選項無法使用
* &amp;lbrack;Bakers&amp;rbrack;SP 中使用的 Mikk 切線空間在 UE4 上無法運作
* &amp;lbrack;Bakers&amp;rbrack; ID 烘焙者無法烘焙材料 ID 顏色
* &amp;lbrack;2D 視圖&amp;rbrack;使用 Geometry 貼紙工具時不會顯示線框圖
* &amp;lbrack;Tool&amp;rbrack;刷子 alpha 通道以檢查器形式顯示，而非材質透明度
* &amp;lbrack;工具&amp;rbrack;幾何貼紙撞擊
* &amp;lbrack;Layers&amp;rbrack;材料槽預設會在填充圖層上摺疊
* &amp;lbrack;Export&amp;rbrack;匯出時超出貼圖集解析度時會當機
* 鏡面通道在濾鏡中無法辨識。
* 清理 + 儲存並不會正確從 SPP 檔案庫中提取資源
* 不要把低多邊形轉換存進高多邊形 assbin 檔案裡
* FBX 檔案匯入了太多貼圖集

**修正：**

* 效果：預設應該開啟音量夾，以模擬「經典」關卡
* 層次：在填土動作中調整最小與最大耕作
* 圖層：儲存並還原堆疊狀態
* 烘焙師：AO Baker 如果沒有指定生命值，請考慮法線貼圖
* 烘焙師：烘焙視窗新增提示與額外資訊
* 儲存專案時建立備份檔案

### 1.3.3

*（發行日期：2015年4月1日）*

**補充：**

* 在標題欄新增軟體版本和專案名稱
* 淨化材質集名稱與智慧材質名稱
* 更新 Substance 引擎至 V5
* &amp;lbrack;Shelf&amp;rbrack;新增環境地圖：科西嘉海灘、Studio 05、Tornoco 工作室等
* &amp;lbrack;Shelf&amp;rbrack;更新MG面罩建構器，加入新參數
* &amp;lbrack;Shelf&amp;rbrack;更新與校正舊環境地圖

**修正：**

* 開啟匯出視窗時當機
* 當 UI 小工具脫離底座時，根本無法拖放
* 「檢查更新」無法運作
* &amp;lbrack;Layers&amp;rbrack;做 ALT+點擊時不要選擇遮罩
* &amp;lbrack;工具&amp;rbrack;三平面無法與 Normal 通道合作
* &amp;lbrack;3D 視圖&amp;rbrack;環境貼圖的漫射光照不正確
* &amp;lbrack;3D View&amp;rbrack;曝光計算與 Designer 不同
* &amp;lbrack;3D 視圖&amp;rbrack;陰影不應該在100%金屬表面上可見
* &amp;lbrack;3D View&amp;rbrack;帶有鏡像 UV 的網格會翻轉切線/雙項式
* &amp;lbrack;3D 視圖&amp;rbrack;陰影會在某些網格上產生錯誤結果
* &amp;lbrack;Bakers&amp;rbrack; 移除由 assbin 檔案建立的「.alg_meta」資料夾
* &amp;lbrack;Bakers&amp;rbrack;烘焙時如果 Painter 同時重新計算 TextureSet，則會當機
* &amp;lbrack;Mac&amp;rbrack;啟動應用程式時的白色盒子介面故障

### 1.3.2

*（發行日期：2015年3月6日）*

**修正：**

* &amp;lbrack;3D View&amp;rbrack;無法重新載入隨專案儲存的環境貼圖

### 1.3.1

*（發行日期：2015年3月5日）*

**補充：**

* &amp;lbrack;Bakers&amp;rbrack;新增快取版本的高多邊形網格以加速計算
* &amp;lbrack;Bakers&amp;rbrack;如果沒有載入高多邊形網格，請新增警告圖示
* &amp;lbrack;Bakers&amp;rbrack;如果沒有載入高多邊形網格，請改用專案網格

**修正：**

* &amp;lbrack;Bakers&amp;rbrack;編輯滑桿值時按下「enter」，關閉視窗
* &amp;lbrack;Bakers&amp;rbrack;啟用/停用烘焙師也會觸發按鈕
* &amp;lbrack;Bakers&amp;rbrack;如果你用「全部/全無」按鈕，根本無法烘焙
* &amp;lbrack;Bakers&amp;rbrack;麵包師按鈕的排序順序不正確
* &amp;lbrack;Bakers&amp;rbrack; 的勾選框被忽略，所有烘焙師都會被處理
* &amp;lbrack;Bakers&amp;rbrack;固定進度條進度

### 1.3.0

*（發行日期：2015年3月4日）*

**補充：**

* &amp;lbrack;Bakers&amp;rbrack;&amp;lbrack;3D View&amp;rbrack;若未找到切線/雙正規性，則使用 Mikkt 切空間計算
* &amp;lbrack;Bakers&amp;rbrack;新增烘焙器：法線、內徑、遮蔽、曲率、厚度、位置
* &amp;lbrack;Effects&amp;rbrack;效果堆疊現在是倒置的，並從上到下顯示（像圖層一樣）
* &amp;lbrack;Effects&amp;rbrack; 在效果堆疊上新增圖示
* &amp;lbrack;Effects&amp;rbrack; 在效果堆疊中加入填充動作間的混合模式
* &amp;lbrack;Effects&amp;rbrack; 重新命名效果（substance effect = filter等）
* 在存檔過程中新增一個「鎖定」檔案
* &amp;lbrack;Effects&amp;rbrack; 在效果堆疊中加入填充動作
* 新增資源：智慧材料
* &amp;lbrack;Layers&amp;rbrack; 允許重新排序層效果
* &amp;lbrack;Tool&amp;rbrack; 新增三平面投影
* &amp;lbrack;3D View&amp;rbrack; 新增陰影支援
* &amp;lbrack;3D View&amp;rbrack;能將所需的 OpenGL 狀態設定為自訂著色器
* &amp;lbrack;3D 檢視與 rbrack;透過新著色器支援 alpha
* &amp;lbrack;3D 檢視與 rbrack;著色器現在已版本化並完整儲存在專案中
* &amp;lbrack;3D View&amp;rbrack;如果著色器不再編譯，請提醒使用者

**修正：**

* &amp;lbrack;Layers&amp;rbrack; fix drop 置於摺疊資料夾下方
* &amp;lbrack;Shelf&amp;rbrack;修正迷你書架中的內容過濾
* &amp;lbrack;Shelf&amp;rbrack;重新命名分類並重新組織分頁

### 1.2.1

*（發行日期：2015年2月12日）*

**補充：**

* \*.spp 檔案現在可以透過在檔案總管中雙擊開啟
* &amp;lbrack;Export&amp;rbrack;新的「$project」標籤用於匯出預設
* &amp;lbrack;Export&amp;rbrack; 在每個材質集下方加入地圖列表（含命名法）
* &amp;lbrack;Export&amp;rbrack; 新增一個按鈕 All/None 來選擇材質集
* &amp;lbrack;Export&amp;rbrack;空地圖在匯出時會被丟棄

**修正：**

* &amp;lbrack;Export&amp;rbrack;Unity5 預設有反轉映射
* &amp;lbrack;Export&amp;rbrack;在預設名稱中加入斜線會造成檔案損壞
* &amp;lbrack;Export&amp;rbrack;以32位元格式匯出的高度通道被錯誤夾緊
* &amp;lbrack;Export&amp;rbrack;材質集合列表不像專案中那樣排序
* &amp;lbrack;工具&amp;rbrack;背面剔除不再有效
* 路徑中有特殊角色時，存檔功能無法使用

### 1.2.0

*（發行日期：2015年1月28日）*

**補充：**

* 新法線通道允許繪製法線貼圖資料並合併結果
* &amp;lbrack;Export&amp;rbrack;新增匯出視窗，可建立自訂包裝並設定自訂名稱
* 專案檔案格式現在由資料夾改為單一檔案
* &amp;lbrack;Export&amp;rbrack;支援不同的 Normal 格式（DirectX、OpenGL）
* &amp;lbrack;Export&amp;rbrack;在匯出時建立一個臨時的「鎖定」檔案
* &amp;lbrack;Layers&amp;rbrack;Shift+左滑鼠點擊可用來切換遮罩
* &amp;lbrack;Parameters&amp;rbrack;在影像輸入底部暴露色彩空間
* &amp;lbrack;Shelf&amp;rbrack; 效果「機槍面罩建造器」現在有新設定
* &amp;lbrack;3D 視圖&amp;rbrack;環境遮蔽圖現在遮蔽的是擴散貢獻，而非鏡面

**修正：**

* 投影材質/模板預覽在視窗中無法正確顯示
* &amp;lbrack;3D View&amp;rbrack;使用「S」（模板）捷徑時不會顯示捷徑提示
* &amp;lbrack;Shelf&amp;rbrack;效果「MatFx 皮膚鱗片」現在在低解析度下表現更好
* &amp;lbrack;Export&amp;rbrack;當指定較大文件大小時，匯出的材質只是放大

### 1.1.2

*（發行日期：2015年1月15日）*

**補充：**

* 新增：填充圖層中的新的平移、旋轉與縮放設定
* 筆刷與填充層的強化濾波
* 試用版現在功能完整（可以匯出），但時間有限。

**修正：**

* 無法用非常小的精度匯入 OBJ 網格
* 在 Windows 7 和 8 啟用授權時遇到的問題
* 專案「另存新檔」時當機
* 刪除貼圖集最後一個通道時會當機
* 在特定情境下刪除圖層時會當機

### 1.1.1

*（發行日期：2014年12月25日）*

**補充：**

* &amp;lbrack;Layer&amp;rbrack;開啟專案/切換貼圖集時，選擇最上層的圖層
* 透過新壓縮演算法提升「儲存」與「另存為」速度
* 開啟對 Painter 來說太近期的專案時會錯誤顯示

**修正：**

* &amp;lbrack;Tool&amp;rbrack;幾何貼紙會產生記憶體損毀
* &amp;lbrack;Brush&amp;rbrack;無法手動輸入筆刷大小低於 1 的浮點值
* &amp;lbrack;Layer&amp;rbrack;建立色彩選擇效果不會把它加入圖層堆疊中
* &amp;lbrack;Layer&amp;rbrack;將滑鼠移到圖層上，Painter 會快速切換工作列
* &amp;lbrack;Layer&amp;rbrack;將位圖當作遮罩可能會導致當機
* Height 通道的單人模式 GUI 不正確
* 「儲存專案」可能會失敗並損壞專案
* 在載入另一個過時著色器的專案後，開啟專案時會當機

### 1.1.0

*（發行日期：2014年12月16日）*

**補充：**

* &amp;lbrack;Effect&amp;rbrack;新材質識別遮罩創建器
* 刷子裝置的新白黑點線
* 新角度跟隨參數
* 新的背面剔除參數
* 新的懶滑鼠參數
* &amp;lbrack;Layers&amp;rbrack;支援多重選擇與管理
* &amp;lbrack;Layers&amp;rbrack; 從一個材質集複製並貼上到另一個
* &amp;lbrack;匯出&amp;rbrack;Adobe Photoshop的PSD格式
* &amp;lbrack;Shelf&amp;rbrack;新工具：毛皮、金屬縫線和拉鍊
* &amp;lbrack;Shelf&amp;rbrack;新刷子：模具、鉛筆、銳線與針法
* &amp;lbrack;Shelf&amp;rbrack;新alpha：高斯噪音、銳利線條、模具、筆、濺花、縫線、拉鍊
* 僅更新部分材質，提升了繪畫效能

**修正：**

* &amp;lbrack;架架&amp;rbrack;不可能載入具有相同標籤的圖表的物質
* &amp;lbrack;Layers&amp;rbrack;通過混合模式無法與遮罩搭配使用
* &amp;lbrack;模板&amp;rbrack;比例在2D視圖中被破壞
* Mac OS Yosemite 的問題與當機

### 1.0.2

*（發行日期：2014年11月9日）*

**補充：**

* 材料預覽中與物質的表現提升
* 更新文件時筆觸預覽的效能提升
* 在非工作區域更新率降低的情況下，視窗效能提升
* &amp;lbrack;Post Effects&amp;rbrack;優化介面以管理設定
* &amp;lbrack;Post Effects&amp;rbrack;重設為預設值
* 在右鍵選單中進行物質效果與圖層操作
* 對物質中預乘輸入/輸出的支持

**修正：**

* &amp;lbrack;3D View&amp;rbrack;自訂著色器參數之間有很大的間隔
* &amp;lbrack;Export&amp;rbrack;缺少 Unity4 預設的 sRGB 轉換
* 載入 fbx 網格時可能當機
* 載入簡單 obj 網格時有時會當機
* 計算條在載入時會被封鎖到 100%
* 重新裝填物質會讓它歸類到所有類別
* DirectX/OpenGL 交換器壞掉了

### 1.0.1

*（發行日期：2014年10月27日）*

**補充：**

* &amp;lbrack;工具&amp;rbrack;改良材料參數使用
* 在說明選單中新增 uservoice 網站的捷徑
* 引擎的各種性能改進

**修正：**

* 粒子的參數值限制在小數點數 2 位
* 從快取載入的物質在介面中不會顯示為過時
* 從網路網址載入網狀網路時會當機
* Painter 現在被識別為已簽署於 Mac OS X 上

### 1.0.0

*（發行日期：2014年10月15日）*

**補充：**

* 自訂著色器支援
* 支援 4K 解析度
* 角色專案範例
* 顯示進度條以應付長時間計算
* &amp;lbrack;Export&amp;rbrack;在擴散後處理前加入一個膨脹通道
* SP 中用於簡單操作的命令列參數
* 新材料與效應
* 工具預覽（即時材料預覽與筆觸測試區分開）
* Painter 啟動時不要建立預設文件
* &amp;lbrack;Tool&amp;rbrack;新增手動編輯灰階值的功能
* 模板的各種改進（吸附、重置）
* 粒子現在是繪畫筆、橡皮擦和投影工具的子工具
* &amp;lbrack;3D View&amp;rbrack;在視窗渲染中使用烘焙的 AO
* 將模板控制分成 2D 和 3D 視圖
* 在函式庫中調整小拇指大小
* 搜尋欄位是針對每個視窗專屬的
* 介面調整

**修正：**

* &amp;lbrack;Susbtance&amp;rbrack;開關無法運作
* &amp;lbrack;色彩對話&amp;rbrack;色調漸層未重新整理
* 如果檔名完全相同，就無法更新網格
* 工具在視圖中無法顯示，當太小時
* Retina 顯示器上的貼花工具無法正常運作
* &amp;lbrack;Substance&amp;rbrack;Int1 顯示為 float1
* &amp;lbrack;Substance&amp;rbrack;底色輸入/輸出無法辨識
* &amp;lbrack;物質&amp;rbrack;過濾器無法重新裝填
* &amp;lbrack;Tool&amp;rbrack;灰階小工具總是會摺疊

## 測試版

### 0.12.1-beta

*（發行日期：2014年9月18日）*

**補充：**

* Unity 5 匯出預設

**修正：**

* PBR 著色器，渲染品質應該會大幅提升
* 對焦功能壞掉了，網格預設會被裁切

### 0.12.0-beta

*（發行日期：2014年9月17日）*

**補充：**

* 滴管工具
* 在網格重新匯入時新增了「保留筆劃位置」選項，方便邊界框改變時使用。
* Cymourai 預設網格的法線貼圖
* 改善工具檢視介面（顏色尚未完成）
* 把選單「幫助->設定」移到「編輯->設定」
* 把匯出路徑存到「匯出所有頻道」視窗裡
* 新關卡 GUI 附直方圖顯示
* 更好的資產管理（拖放、重新載入資源、刪除未使用的）
* 從「漫反射」切換到「底色」
* 滑桿編輯調整 - 允許除逗號外加點
* 填充層：增加最大平鋪值
* 預設環境地圖

**修正：**

* 極端角度下的不良反射偽影
* 斷裂的鏡面/光澤輸出
* 畫家「關於」視窗中的連結無法使用
* 與 OSX 優勝美地的撞機
* 網格是用三角定位儲存的
* 工具視窗的色彩捷徑是傳送到發射器，而不是灰階
* 切換圖層到遮罩時，顏色選擇器會保持開啟
* 無法從填充層保存材質
* 可調整書架三個區域的大小

### 0.11.0-beta

*（發行日期：2014年9月4日）*

**補充：**

* 在 3D 和 2D 視圖之間加一個分線器
* 在 2D/3D 視圖中使用漸層背景
* Levels 直方圖介面
* 合併書架與圖書館
* 建立或更新預設時不需要存檔動作
* 透過拖放方式匯入架上的資產

**修正：**

* 按鈕名稱顯示在主工具列

### 0.10.2-beta

*（發行日期：2014年8月28日）*

**修正：**

* 匯出所有通道會產生錯誤的結果

### 0.10.1-beta

*（發行日期：2014年8月26日）*

**修正：**

* 著色器呈現黑色且粗糙度低的結果
* GPU 檢查：處理「Quadro」卡，偵測所有裝置並相應調整使用者訊息
* 大多數物質材料在Beta 9中限制在256
* 匯出為點陣圖時，高度會被夾住
* 筆刷預覽和 Mac 上的投影疊加不同
* 使用 Geometry 工具建立遮罩時，視窗裡不會顯示
* 快速面具壞了
* 修正舊版 Mac Pro 的混合問題

### 0.10.0-beta

*（發行日期：2014年8月7日）*

**補充：**

* 模板遮罩

**修正：**

* Quadro 卡支援
* 著色器呈現黑色且粗糙度低的結果
* 物質含量上限為256
* 法線貼圖匯出會刪除綠色通道

### 0.9.0-beta

*（發行日期：2014年7月17日）*

**補充：**

* Yebis 2 後製
* 新專案精靈允許你匯入輸入映射（AO、曲率等）。
* 自動插入輸入映射（AO、曲率等） 至物質效應
* 對材料的縮放控制，應用於填充層

### 0.8.2-beta

*（發行日期：2014年7月11日）*

**修正：**

* 色調滑桿預設為白色
* 若材質名稱包含特殊字元，專案重置
* 單一材質物件的材質名稱變更不應該使專案失效。
* 儲存專案後重新開啟 UV 就會出問題

### 0.8.1-beta

*（發行日期：2014年7月4日）*

**修正：**

* 多次顯示卡當機
* 匯出頻道時當機

### 0.8.0-beta

*（發行日期：2014年6月28日）*

**補充：**

* 多材質 - 你現在可以在同一份文件中同時繪製多種材質
* 對稱繪畫
* 所有混合模式現已開放

**修正：**

* 多次顯示卡當機
* 若材質名稱包含特殊字元，專案重置
* 儲存專案後 UV 會出問題，重新開啟時會有多個 UV

### 0.7.0-beta

*（發行日期：2014年6月18日）*

**補充：**

* 圖層效應
* 新物質模板材料
* 透明面罩
* 允許複製/貼上圖層/遮罩
* Allwo 轉為複製層
* 編輯圖層遮罩時更換工具
* 物質現在是用GPU驅動的

**修正：**

* 高度圖繪製不會繪製負值。
* 材質選擇器的顯示不應考慮取樣的法線貼圖
* 粒子決定論被打破
* 二維視圖中的模板矩陣
* obj 檔案中的 Ngon
* 各種墜機事件

### 0.6.0-beta

*（發行日期：2014年6月4日）*

**補充：**

* 新增匯出選項，可從粗糙度與金屬通道合成中匯出鏡面貼圖

**修正：**

* Windows Vista 相容性
* 高度圖不會繪製負值

### 0.5.0-beta

*（發行日期：2014年5月7日）*

**補充：**

* 3D/2D 視角切換器
* UV 區塊選擇工具
* 在遮罩上繪畫時，工具會自動更換。
* 物質的解決取決於文件的

**修正：**

* 發射時墜毀
* ASCII 網格當機
* 二維視圖中的固定模板矩陣
* 與橡皮擦撞車

### 0.4.0-beta

*（發行日期：2014年4月17日）*

**補充：**

* 無縫 2D 視圖
* 位圖圖層遮罩
* 環境暴露控制
* 填充圖層現在會透過工具視窗來設定屬性
* 材料可應用於填充層
* 在模板庫中新增了更多模板
* 粒子預設更新以加快計算速度
* PBR 著色器優化與低品質設定的品質提升

**修正：**

* 圖層縮圖會連結到目前選擇的通道
* 經常當機

### 0.3.0-beta

*（發行日期：2014年4月4日）*

**補充：**

* 在色彩選擇器中允許負值來繪製高度圖
* 預覽所選材質/顏色
* 在工具列中新增工具快捷鍵（1、2、3、4）
* 在專案中全域切換 Normal 格式（OpenGL 與 DirectX 不同）
* 新專案精靈
* 間距滑桿不再被夾緊
* 更新的滑桿風格
* 讓選色器非模態
* 選擇材料進入函式庫時，會相應地設定工具類型

**修正：**

* 已修正：匯入網格路徑不會被保留
* 已修正：錯誤的材質生成
* 已修正：啟動時當機

### 0.2.0-beta

*（發行日期：2014年3月17日）*

**補充：**

* 材料滴管（P 捷徑）
* 3D 工具預覽下方的縮圖
* 獨立版本的授權系統
* &amp;lbrack;以及 &amp;rbrack;筆刷大小的快捷鍵
* 匯出地圖上的填充
* 更新後的工具視窗樣式
* 更新的滑桿風格
* 更新的預設 HDR 環境

**修正：**

* 模板：3D 視圖中的變動流量值停止於 52
* 在行程中加入 0 壓力鍵時，引擎中的無限迴圈是固定的
* 工具：角度抖動無法回傳超過 +/- 90% 的數值
* 選取圖層遮罩時，3D 視圖顯示會改變
* 反向變焦

### 0.1.0-beta

*（發行日期：2014年3月2日）*

**補充：**

* 新圖書館管理
* 新筆刷與粒子內容
* 3D 筆刷預覽
* 更新後的工具視窗樣式
* 更新的滑桿風格
* 更新的快取效能

**修正：**

* 攝影機控制
* 刷子旋轉
