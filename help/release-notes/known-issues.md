---
helpx_url: 'https://helpx.adobe.com/substance-3d-painter/release-notes/know-issues.html'
breadcrumb-title: ''
description: 檢視 Substance 3D Painter 已知的問題，以掌握最新版本的限制與解決方法。
helpx_creative_field: ''
helpx_description: Substance 3D Painter
helpx_experience_level: ''
helpx_learn_topic: ''
helpx_tags: ''
title: 已知問題
user-guide-description: ''
user-guide-title: ''
source-git-commit: c95676d7a6269addb3a0b42ab671a649a93caa10
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 0%

---


# 已知問題

本頁列出 Substance 3D Painter v12.1.0 中所有已知的活躍問題：

* `[Engine]` 使用 Smart Materials 時，若材質集沒有圖塊 1001，則會出現錯誤
* `[Engine]` 用克隆工具在正常通道中繪製顏色移位錯誤
* `[Engine]` 幾何遮罩在 UV 邊界與實例圖層會顯示雜訊
* `[Engine]` UV 填充「3D 空間鄰居」模式在細三角形上效果不佳
* `[Engine]` 錨點結果不會在遮罩和色彩通道之間渲染

* `[Baking]` 簡單方塊上的AO錯誤
* `[Baking]` 以姓名匹配後綴的解釋是錯誤的
* `[Baking]` MES 重新進口後，UV 接縫就不會出現了
* `[Baking]` 帶有某些設定的網格狀雜訊

* `[Substance]` 資源中多次拼寫錯誤
* `[Substance]` 空白區破壞可見性條件
* `[Substance]` 某些材質的預設載入時間太慢
* `[Substance]` 無法以混合用途匯入資源

* `[Color Management]` 與未用於遮罩的產生器不相容的綁定
* `[Color Management]` 濾波器輸出未被妥善考慮
* `[Color Management]` 在 Linux 上使用 ACE 進行 HDR 色彩空間轉換會產生壓縮色彩

* `[Shelf]` 如果資源被放在有特定名稱的資料夾裡，就會被錯誤使用。
* `[Shelf]`&#x200B;`[Substance]`用戶資料未被納入架上縮圖生成。

* `[Shader]` 「camera_vp_matrix_inverse」參數未被識別
* `[Shader]` user0 通道在特定著色器下永遠無法被讀取為 sRGB

* `[Scripting]`&#x200B;`[Javascript]` 在輸出函式中指定抖動參數時出現「Disbaled」的錯字
* `[Scripting]`&#x200B;`[Python]` substance_painter.project 模組中的各種錯字

* `[Single Channel View]` 在 Painter 版本更新後，專案儲存在基礎色彩檢視中看起來變暗了
* `[Single Channel View]` 在 Painter 版本更新後，專案儲存在基礎色彩檢視中看起來變暗了

* `[gltf]` 無法打開透過 Babylon Exporter 匯出的檔案
* `[Displacement]` 上色時的故障
* `[Polygon Fill Tool]` 對稱性錯誤選擇
* `[2D view]` 繪畫時有時不會出現筆觸
* `[Console]` 無法寫出與捷徑相關的符號
* `[LOG]` 匯出失敗時錯誤訊息
* `[3D View]` 模板對複製物體無效
* `[Resource updater]` 書架上同名的不同資源會被當作一個資源讀取
* `[Sample]` 預覽範例中的壞掉相機
* `[Instancing]`&#x200B;`[Projection]`在平面程序中選擇一個實例時，會在另一個貼圖集合上選擇另一個平面程序
* `[Slider]` 當游標離開視窗時，數值輸入會被取消選擇
* `[Anchor point]` 複製貼上 Mask 內容時的引用失效
* `[Mesh export]` 不要考慮新的材質集名稱
* `[Anchor Points]` 在發電機中使用時顏色錯誤
* `[Bakers]` ID Map Baker 不考慮 3ds Max 2021 實體資料
* `[UV Tiles]` 沒有針對特定網格重疊的 UV 空間錯誤訊息
* `[GLTF]`&#x200B;`[Crash]`建立壓縮 gltf 檔案的專案會導致當機
* `[UV Tile sequence]` 位置圖沒有正確匯入
* `[UVTiles]` 高度組合遮罩不會用 UV Tile 遮罩重新整理
* `[Import]` 無法匯入帶有「nan」值的obj檔案
* `[Export]` GLTF 匯出的大小錯誤
* `[Texture Set]` 名稱可以是空的
* `[Layer stack]` 複製到遮罩後切換到材質模式
* `[UI]` 刷具製作機設定中的打字錯誤
* `[Texture Set Settings]` 重新命名後著色器實例名稱錯誤
* `[Blending]` 色彩和飽和度混合模式也會改變亮度
* `[Librairies]` 已儲存搜尋的寬度與路徑篩選視窗在更改時未被儲存
* `[Geometry mask]` 重新匯入網格和實例圖層時的問題
* `[Color management]` 當圖塊 1001 遺失時，找不到色彩空間
* `[Export mesh]` 位移未匯出特定 UV 圖塊
* `[RedHat]` 色彩選擇器問題
* `[Regression]`&#x200B;`[UI]`右鍵選單在高清螢幕上太小了
* `[Resources]` 匯入的網格貼圖會被自動更新忽略
* `[User Channels]` 色彩混合空間預覽錯誤
* `[Mask]` 切換到烘焙模式後，幾何選擇仍然有效
* `[Sonoma]` 圖示不會出現在選單中
* `[Path]` 高度混合多條路徑會導致雜訊
* `[USD]` 有些情況下是錯誤的 USDA 分配
* `[Polygon Fill]` 更改基底色的色彩空間不會更新色彩選擇器
* `[Paint Skew]` 切換到繪畫模式後，繪圖斜向中選取的工具仍保持選取
* `[Color Picker]` 換工具後，撥片器仍保持開啟
* `[UV Padding]` 在匯出時將貼圖從 4k 升頻到 8k 時出現的瑕疵
* `[Baking Common Settings]` 籠子距離設定不會更新籠子線框和著色器視覺化
* `[Send to Photoshop]` 無法匯出圖層遮罩
* `[Skew Baking]` 在上色和解除時，傾斜修正會斷裂
* `[Projection Tool]` 投影工具阻擋了視窗互動
* 非正方形資源在刷子通道槽中使用時會被拉伸
* 未能解碼實質內容
* 非完美疊加的紫外線可能會產生瑕疵
* 帶有部分 FBX 的網格法線無效
* 當切換受關卡影響的頻道時，視圖不會更新
* 只有一個貼圖集的專案會在 Base Color 單獨模式下重新開啟
* 材質/繪畫屬性中通道按鈕的介面可能會壞掉
* 屬性中通道的順序可以被打破
* L16F 和 RBG16F 製作的筆劃可能會顯示瑕疵
* 還原按鈕的行為不會與相機設定中的鎖定鍵互動
* Photoshop 匯出會忽略幾何遮罩的選取
* 模糊斜率和變形濾鏡取決於材質集的解析度
* 沒有名稱的地圖則是在匯出資料夾外建立的
* 更改筆刷預設時，模板不會更新
* PSD 檔案透明度的問題
* 從上下文工具列修改的筆刷參數不會出現在歷史紀錄中
* 如果你這次已經刪除並重新建立匯出預設，就無法重新命名或刪除它
* 有些情況下，投影工具預覽的頻道映射無法運作。
* 開啟和保存某些專案可能會比平常花更長時間。

## 穩定性

* `[Crash]` 在建立專案失敗後點擊貼圖集列表會導致當機
* `[Crash]` 當同一專案同時開啟兩次時，嚴重錯誤當機
* `[Crash]` 當網格載入失敗時，選擇「匯出網格」
* `[Crash]` 嘗試開啟舊專案後點選「開始繪畫」
* `[Crash]` 在 Ribbon 中建立非常長的文字可能會當機
* `[Crash]` 裝置在烘焙時遺失後回到繪畫模式
* `[Crash]` 取消地圖後退出畫家 匯出
* `[Crash]` 匯出帶有相機名稱中特殊符號的網格
* `[Crash]` 在遮罩檢視模式下刪除頻道會導致當機
* `[Crash]` 某些物質在製造時可能導致崩潰
* `[Crash]` 烘焙模式下重新匯入網格
* `[Crash]` 重新裝填多個網格可能會導致當機
