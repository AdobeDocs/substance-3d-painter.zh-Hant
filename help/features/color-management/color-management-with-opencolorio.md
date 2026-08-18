---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/features/color-management/color-management-with-opencolorio.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中使用 OpenColorIO 色彩管理，以實現跨管線的色彩工作流程一致。
helpx_creative_field: ""
helpx_description: Painter > Features > Color management > Color management with OpenColorIO
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: OpenColorIO 的色彩管理
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '675'
ht-degree: 0%

---


# OpenColorIO 的色彩管理

本頁列出與 OpenColorIO（OCIO）相關的色彩管理設定。

## 專案設定

![](../../assets/project-settings-3.png)

專案設定可在新專案視窗建立新專案[](../../getting-started/project-creation.md)時設定，或使用[專案設定](../../interface/project-configuration.md)視窗設定。

>[!NOTE]
>
> 如果 **OCIO** 環境變數存在，且指定有效的設定檔，它會在 UI 中覆寫並停用設定。

可用的設定如下：

<table data-preserve-html="true" style="width: 99.9039%;"><colgroup><col style="width: 12.512%;"/><col style="width: 21.1742%;"/><col style="width: 66.3122%;"/></colgroup><tbody><tr><th style="width: 12.5%;">章節</th><th style="width: 21.1538%;">背景設定</th><th style="width: 66.25%;">說明</th></tr><tr><td rowspan="3" style="width: 12.5%;"><strong>配置</strong></td><td style="width: 21.1538%;"><strong>色彩管理</strong></td><td style="width: 66.25%;"><p>定義用哪個引擎來管理顏色。</p><p>可能的數值：</p><ul><li><strong>舊有</strong> （預設）：使用預設的 sRGB/Linear sRGB 伽瑪色彩校正。</li><li><strong>OpenColorIO</strong>：使用 OCIO 整合。</li><li><strong>Adobe ACE</strong>：Adobe 色彩引擎，以支援 ICC 設定檔。</li></ul></td></tr><tr><td style="width: 21.1538%;"><strong>OpenColorIO 設定</strong></td><td style="width: 66.25%;"><p>該用哪個設定檔來驅動色彩管理設定。</p><p>可能的數值：</p><ul><li><strong>物質</strong> （預設）：使用線性伽瑪作為工作空間。</li><li><strong>ACES 1.0.3</strong>：使用 ACEScg 作為工作空間。</li><li><strong>ACES 1.2</strong>：使用 ACEScg 作為工作空間。</li><li><strong>自訂</strong>：使用自訂設定檔。</li></ul></td></tr><tr><td style="width: 21.1538%;"><strong>設定檔</strong></td><td style="width: 66.25%;">通往 OCIO 設定檔的路徑。 若設定模式未設為 <strong>自訂</strong>，則會被停用。</td></tr><tr><th style="width: 12.5%;"><br/></th><th style="width: 21.1538%;"><br/></th><th style="width: 66.25%;"><br/></th></tr><tr><td rowspan="2" style="width: 12.5%;"><strong>色彩設定</strong></td><td style="width: 21.1538%;"><strong>工作色彩空間</strong></td><td style="width: 66.25%;">引擎在應用程式內部使用的色彩空間。 這是材質可以轉換成（匯入）或從（匯出）的色彩空間。</td></tr><tr><td colspan="1"><strong>標準 sRGB 色彩空間</strong></td><td colspan="1"><p>色彩空間與[標準sRGB]（https://en.wikipedia.org/wiki/SRGB）色彩空間（IEC 61966-2-1：1999）相符。</p><p>這個色彩空間在應用程式的多個地方被使用：</p><ul><li>要將色彩集合轉換成色彩選取器的十六進位欄位。</li><li>在色彩選擇器中儲存並載入色片。</li><li>在色彩選擇器列表中被列為顯示。</li></ul></td></tr><tr><th style="width: 12.5%;"><br/></th><th style="width: 21.1538%;"><br/></th><th style="width: 66.25%;"><br/></th></tr><tr><td rowspan="4" style="width: 12.5%;"><strong>點陣圖匯入色彩空間預設值</strong></td><td style="width: 21.1538%;"><strong>8 位元影像</strong></td><td style="width: 66.25%;">匯入 8 位元影像檔案時預設使用的色彩空間。</td></tr><tr><td style="width: 21.1538%;"><strong>16位元影像</strong></td><td style="width: 66.25%;">匯入 16 位元影像檔案時預設使用的色彩空間。</td></tr><tr><td style="width: 21.1538%;"><strong>浮點影像</strong></td><td style="width: 66.25%;">匯入 HDR/EXR 影像檔案時預設使用的色彩空間。</td></tr><tr><td style="width: 21.1538%;"><strong>自動偵測色彩空間</strong></td><td style="width: 66.25%;"><p>允許根據特定設定從資源中定義色彩空間。</p><p>可能的數值：</p><ul><li><strong>停用</strong>：使用預設色彩設定，忽略資源設定。</li><li><strong>解析檔名</strong> （預設）：使用 OCIO [命名慣例]（https://opencolorio.readthedocs.io/en/latest/guides/authoring/rules.html?highlight=filename#strictparsing） 來擷取資源所使用的色彩空間名稱。</li><li><strong>使用設定檔規則</strong>：使用 OCIO 設定來決定如何分配色彩空間。 此參數優先於先前影像檔案的色彩空間設定。</li></ul></td></tr><tr><th style="width: 12.5%;"><br/></th><th style="width: 21.1538%;"><br/></th><th style="width: 66.25%;"><br/></th></tr><tr><td style="width: 12.5%;"><strong>物質材料</strong></td><td style="width: 21.1538%;"><strong>材質色彩空間預設</strong></td><td style="width: 66.25%;"><p>定義 Substance 材質色彩管理輸入/輸出的色彩空間（頻道列表見下方）。</p></td></tr><tr><th style="width: 12.5%;"><br/></th><th style="width: 21.1538%;"><br/></th><th style="width: 66.25%;"><br/></th></tr><tr><td rowspan="3" style="width: 12.5%;"><strong>匯出色彩空間</strong><br/><br/><br/></td><td style="width: 21.1538%;"><strong>8 位元影像</strong></td><td style="width: 66.25%;">匯出 8 位元影像檔案時預設使用的色彩空間。</td></tr><tr><td style="width: 21.1538%;"><strong>16位元影像</strong></td><td style="width: 66.25%;">匯出 16 位元影像檔案時預設使用的色彩空間。</td></tr><tr><td style="width: 21.1538%;"><strong>浮點影像</strong></td><td style="width: 66.25%;">匯出 HDR/EXR 影像檔案時預設使用的色彩空間。</td></tr></tbody></table>

### OpenColorIO 角色

以下角色支援，並允許更改預設的色彩空間選擇：

| 角色名稱 | 說明 |
| --- | --- |
| **內容\_3d\_painter\_standard\_srgb** | 指定與標準 sRGB](https://en.wikipedia.org/wiki/SRGB) 相符[的色彩空間（IEC 61966-2-1：1999）。 |
| **實質_3d\_painter\_bitmap\_import\_8bit** | 用 Role 來指定匯入 8 位元影像所使用的色彩空間。 |
| **內容\_3d\_painter\_bitmap\_import\_16bit** | 用 Role 指定匯入 16 位元影像所使用的色彩空間。 |
| **實質_3d\_painter\_bitmap\_import_floating** | 用 Role 指定匯入 HDR 影像所使用的色彩空間。 |
| **內容\_3d\_painter\_substance\_material** | Role 用來指定 Substance 材質中色彩管理通道所使用的色彩空間。 |
| **實質\_3d\_painter\_bitmap\_export\_8bit** | 用 Role 來指定匯出 8bit 貼圖時所使用的色彩空間。 |
| **內容\_3d\_painter\_bitmap\_export\_16bit** | 用 Role 來指定匯出 16 位元貼圖時使用的色彩空間。 |
| **內容\_3d\_painter\_bitmap\_export\_floating** | 用 Role 來指定匯出 HDR 貼圖時使用的色彩空間。 |

>[!NOTE]
>
> 應用程式提供的 OCIO 配置可作為如何使用這些特定角色的範例。
