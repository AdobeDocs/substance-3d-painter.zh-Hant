---
helpx_url: 'https://helpx.adobe.com/substance-3d-painter/interface/project-configuration.html'
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中設定專案設定，以設定材質解析度、通道和專案屬性。
helpx_creative_field: ''
helpx_description: Painter > Interface > Project configuration
helpx_experience_level: ''
helpx_learn_topic: ''
helpx_tags: ''
title: 專案配置
user-guide-description: ''
user-guide-title: ''
source-git-commit: 3e4ef9bd5897f042b01d6c0819ec06cc21ba208a
workflow-type: tm+mt
source-wordcount: '839'
ht-degree: 0%

---


# 專案配置

![](../assets/project-configuration-full.png)

專案設定視窗中有修改專案設定的控制。 專案設定通常會在建立新專案時設定，但有時在專案後期可能需要調整這些設定。

## 3D 網格

如果 3D 網格或網格檔案有變動，你可以重新匯入網格，同時保留其他專案資料。 檢查 **Reimport mesh** ，確保匯入的是正確的檔案。

重新匯入網格通常很有用，當你需要：

* 更新 3D 模型拓撲
* 更新 UV
* 新增或移除 [貼圖集](texture-set/texture-set.md)

| **參數** | **描述** |
| --- | --- |
| **3D 網格** | 指示 3D 模型檔案的路徑。 使用 **Select 按鈕** 來更改專案的原始檔案。 |
| **重新匯入網格** | 如果啟用了，點擊介面底部的確定時，網格檔案會重新匯入。 如果使用 Select 按鈕指定與原始網格檔案不同的網格檔案，該參數會自動被勾選。 |

>[!NOTE]
>
> 如果在重新匯入專案網格時材質 ID 改變或被重新命名，專案中先前的貼圖集可能會被停用，導致看起來像是缺少貼圖。 這可以透過材質集合列表中&#x200B;**的重新指派視窗**](texture-set/texture-set-reassignment.md)來修正[。

## 專案設定

此區控制與專案相關的多項設定：

<table>
  <tr>
    <th><em>背景設定</em></th>
    <th><em>說明</em></th>
  </tr>
  <tr>
    <td><strong>法線貼圖格式</strong></td>
    <td>定義了視窗中網格所使用的法線貼圖格式。 這個參數只影響<a href="shader-settings/shader-settings.md">視窗中的著色器和</a>烘焙器的</a>網格貼圖<a href="../baking/baking.md">。層堆疊是獨立的。 常見應用的建議值：<br><br><ul><li><strong>Unity</strong> 版：OpenGL</li><li><strong>Unreal 引擎</strong>：DirectX</li><li><strong>Maya</strong>：OpenGL</li><li><strong>3DS Max</strong>：DirectX</li><li><strong>Blender</strong>：OpenGL</li></ul></td>
  </tr>
  <tr>
    <td><strong>計算每個片段的切空間</strong></td>
    <td>決定如何在視窗中計算並顯示陰影與光照的法線貼圖。 啟用後，網格的切線與雙法線會以像素計算，而非頂點計算。<br>常見應用的建議值：<br><br><ul><li><strong>Unity</strong>：停用（使用 HDRP 則啟用）</li><li><strong>Unreal 引擎</strong>：啟用</li></ul></td>
  </tr>
</table>

>[!NOTE]
>
> 更改法線格式或切線計算需要重新烘焙網格貼圖，以確保視窗中的外觀正確。

### 檔案類型專屬設定

當選擇 USD 網格格式時，其他檔案類型的特定設定會開放。

![](../assets/image2023-1-30-11-16-6.png){width="473px"}

<table>
  <tr>
    <th><em>參數</em></th>
    <th><em>說明</em></th>
  </tr>
  <tr>
    <td><strong>範圍與變體</strong></td>
    <td>選擇 USD 檔案中的特定部分。 預設情況下，它設定為「Root」，這表示整個 USD 檔案會被用於 Painter 專案。 <strong>找零......</strong> 會打開一個新視窗，顯示美元內容。 若偵測到變體，您可以選擇特定變體載入專案。<br><br>注意：<br><ul><li>只有模型變體的選擇才會產生影響。</li><li>目前尚未偵測到嵌套於變異中的變異。</li></ul></td>
  </tr>
  <tr>
    <td><strong>分區層級</strong></td>
    <td>適用於有細分的幾何。 在 Painter 裡指定要細分多少網格來做貼圖。 如果 USD 檔案中明確設定為「無」，這個設定會顯示灰色。 細分是在 UV 展開後才套用，因此不會改變網格 UV 的形狀。</td>
  </tr>
  <tr>
    <td><strong>邊框</strong></td>
    <td>適用於偵測到動畫的美元。 選擇將載入 Painter 專案的框架。 如果選取的 USD 檔案中沒有動畫，這個設定會變成灰色。</td>
  </tr>
</table>

## UV 圖塊設定

本區段有切換專案中 UDIM 使用的控制。 專案建立後無法更改這些設定，但你可以在這裡查看專案的設定。 更多資訊請參閱 [UV Tiles 文件](../features/uv-tiles/uv-tiles.md)。

## 匯入設定

這些設定控制選取的網格如何匯入：

| *背景設定* | *描述* |
| --- | --- |
| **進口相機** | 啟用後，網格檔案中的攝影機也會匯入並在 3D 視窗中使用。 |
| **保留網格上的筆劃位置** | 此設定控制匯入新 3D 網格後筆觸如何重新計算。 建議在大多數情況下保持此設定開啟。 更多細節請參閱 [UV 重投影](../features/uv-reprojection.md) 文件。 |
| **自動展開** | 自動紫外線展開。 點擊選項按鈕來設定流程。 更多資訊請參閱 [自動 UV 展開文件](../features/automatic-uv-unwrapping.md)。 |

### 實體尺寸設定

調整 [匯入網格的實體尺寸](../features/physical-size.md) 。

| *背景設定* | *描述* |
| --- | --- |
| **使用 mesh 檔案的內部單位縮放** | 如果網格是用物理上精確的測量建立的，請選擇此選項以維持 Painter 中的相同物理尺寸。 |
| **客製化單位比例** | 如果網格本身沒有考慮到實體尺寸，請使用此選項自訂網格大小。 你需要知道所需的實體尺寸以及匯入網格的單位大小，才能決定這個值。 |
| **指派材料時，切換填充層縮放為實體尺寸** | 啟用後，填充圖層和效果會在指派具有物理尺寸屬性的材質時，自動將縮放方法切換為物理尺寸。 |

### 色彩管理設定

此區控制如何轉換顏色的設定。 欲了解更多資訊，請參閱 [色彩管理](../features/color-management/color-management.md) 文件。
