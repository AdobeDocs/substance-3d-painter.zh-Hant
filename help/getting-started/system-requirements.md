---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/getting-started/system-requirements.html"
breadcrumb-title: ''
description: 請檢視 Substance 3D Painter 的系統需求，確保您的電腦符合硬體與軟體規格。
helpx_creative_field: ""
helpx_description: Painter > Getting Started > System requirements
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 系統需求
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 0%

---


# 支援系統

以下是該應用程式所支援的硬體與系統清單：

## 窗戶

|  | 最低限度 | 推薦 | 最佳 |
| --- | --- | --- | --- |
| <b>作業系統</b> | Windows 11 64 位元版本 23H2 | Windows 11 64 位元版本 24H1 | Windows 11 64 位元版本 24H2 |
| <b>中央處理器</b> | Intel Core i5 AMD Ryzen 5 | Intel Core i7 AMD Ryzen 7 | Intel Core i9 AMD Ryzen 9 |
| <b>GPU</b> | NVIDIA GeForce RTX 2060 超級 NVIDIA Quadro RTX 4000 AMD Radeon RX 5700 XT AMD Radeon Pro W5700 | NVIDIA GeForce RTX 3080、NVIDIA Quadro RTX A4000、AMD Radeon RX 6800 XT、AMD Radeon Pro W7700 | NVIDIA GeForce RTX 4090、NVIDIA Quadro RTX 5000、Ada 世代 AMD Radeon RX 7900、XTX AMD Radeon Pro W7800 |
| <b>VRAM</b> | 8 GB | 16 GB | 24 GB |
| <b>記憶體</b> | 16 GB | 32 GB | 64 GB |
| <b>儲存</b> | SSD 有 30 GB 可用空間 | SSD 有 50 GB 可用空間 | SSD 有 70 GB 可用空間 |

### MACOS

|  | 最低限度 | 推薦 | 最佳 |
| --- | --- | --- | --- |
| <b>作業系統</b> | macOS 12 蒙特雷 | macOS 13 Ventura | macOS 14 Sonoma |
| <b>中央處理器</b> | 蘋果 M1 | 蘋果 M2 Pro | Apple M4 Pro |
| <b>GPU</b> | 蘋果 M1 | 蘋果 M2 Pro | Apple M4 Pro |
| <b>記憶體</b> | 16 GB | 32 GB | 64 GB |
| <b>儲存</b> | SSD 有 30 GB 可用空間 | SSD 有 50 GB 可用空間 | SSD 有 70 GB 可用空間 |

### Linux

| 企業號 | 蒸汽 |
| --- | --- |
| RHEL 8</br>RHEL 9 | Ubuntu 22.04 |

## 一般建議

為了在使用 UV Tile 工作流程時獲得良好效能，我們建議使用：

* 32GB 記憶體
* 配備 8GB 顯存的 GPU
* SSD 用來存放專案快取和應用程式快取。

其他事項：

* 許多 Substance 應用程式依賴 OpenSSL 1.1.1 來相容 RHEL8/9。 對於使用較新版本 OpenSSL 的系統，客戶需手動提供
* 在舒適環境下工作時，我們建議使用垂直解析度超過 1000 像素且寬度超過 1280 像素的螢幕。
* 要以 8K</b>（8192/*8192 像素）匯<b>出，需要一顆超過 <b></b> 2GB VRam 的 GPU。
* 只有 2019.x 及以上版本經過公證，才能在 MacOS 10.15（Catalina）上運行。
* 若要透過遠端桌面（RDP）使用該軟體，請參閱專門的文件 [頁面](../pipeline-and-integration/configuration/remote-desktop.md)。
* Ryzen CPU 烘焙時會當機，可以透過更新 BIOS 來解決。

## 不支援的配置

<b>窗戶</b>

* 不支援虛擬機。
* Windows Server 不支援。

<b>麥克</b>

* 僅支援官方蘋果配置。
* 目前不支援 eGPU，且可能存在穩定性問題。

<b>Linux</b>

* Linux 上的 Mesa 驅動程式不被支援。

<b>任何平台</b>

* 整合式 GPU 不支援 x86-64（Intel、AMD）CPU 的配置。

## 最低 GPU 驅動程式版本

以下是應用程式正常運行所需的最低 GPU 驅動版本清單。 隨著新版本發布，此列表可能會有所變動。

要下載新驅動程式，請參見： [GPU 驅動程式過](../technical-support/technical-issues/gpu-issues/gpu-has-outdated-drivers.md)時。

| 作業系統 | NVIDIA | AMD | 英特爾 |
| --- | --- | --- | --- |
| <b>窗戶</b> | GeForce 442.50 Quadro 442.50 | Radeon 19.7.1 Radeon Pro / FirePro 18.Q4 | 15.33 |
| <b>Linux</b> | 535.171.04 或更晚 | Radeon 22.40.6 | 無支撐 |

>[!NOTE]
>
> 在 Mac OS **上**，GPU 驅動程式是由作業系統本身提供。更新到作業系統最新版本以存取最新的驅動程式。

### 驅動程式相容性問題

關於各建構程式的詳細顯示卡驅動問題清單，請參考 [專門的文件頁面](../technical-support/technical-issues/gpu-issues/gpu-drivers-compatibility.md)。

## GPU 光線追蹤用於烘焙

若要啟用 GPU 光線追蹤，必須安裝上述建議的最低驅動程式。

<b>DXR</b> 也要求以下最低配置：

* <b>Windows 10</b> 版本 1809，請參閱 [此頁面](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/features/gpu-raytracing) 以獲取更多資訊
* <b> 採用 Pascal 架構</b> 的 GPU（Nvidia GeForce 10XX）

>[!TIP]
>
> GPU 光線追蹤在專用光線追蹤硬體上運行最佳，例如 NVIDIA GeForce RTX 或 NVIDIA Quadro RTX GPU。

## 支援的繪圖板

以下是已在 Substance 3D Painter 7.4.2</b> 版本<b>測試過的相容繪圖板清單：

+++Wacom
<b>型號：</b>Intuos Pro（M尺寸）、Intuos（S尺寸）


| 作業系統 | 驅動版本 |
| --- | --- |
| 窗戶 | 6.3.45-1 |
| macOS | 6.3.45-3 |


+++

+++XPen
<b>型號：</b>Deco 01


| 作業系統 | 驅動版本 |
| --- | --- |
| 窗戶 | XP-PENWin\_3.2.2.211027 |
| macOS | XP-PENMac\_3.2.3\_211203 |
| Linux | XP-PEN-pentablet-3.2.1.211019-1 |


+++

+++惠翁
<b>型號：</b>Q11K


| 作業系統 | 驅動版本 |
| --- | --- |
| 窗戶 | XP-PENWin\_3.2.2.211027 |
| macOS | XP-PENMac\_3.2.3\_211203 |


+++

+++Xencelabs
<b>型號：</b>筆型平板中等


| 作業系統 | 驅動版本 |
| --- | --- |
| 窗戶 | XencelabsWin\_1.2.1-14 |
| macOS | XencelabsMac\_1.2.1-18 |
| Linux | XencelabsLinux\_1.1.0-2 |


+++

## 支援的 3Dconnexion SpaceMouse 模型

以下是已在 Substance 3D Painter 8.1 版本<b>測試過的 3Dconnection 太空滑鼠](https://3dconnexion.com/us/spacemouse/)相容驅動版本[列表。</b>

驅動版本適用於 <b>緊湊型</b>、 <b>專業</b> 版及 <b>企業</b> 版。

| 作業系統 | 驅動版本 |
| --- | --- |
| 窗戶 | 10.8.6.3431 |
| macOS | 10.7.2.3454 |

## 語言

軟體介面提供以下語言：

* 英語（美國）
* 德語
* 西班牙語
* 法語
* 義大利語
* 日本
* 韓語
* 葡萄牙語（巴西）
* 中文（簡體）
