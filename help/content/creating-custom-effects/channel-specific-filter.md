---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/content/creating-custom-effects/channel-specific-filter.html"
breadcrumb-title: ''
description: 學習如何為 Substance 3D Painter 製作特定通道的濾鏡效果，以處理個別貼圖通道。
helpx_creative_field: ""
helpx_description: Painter > Content > Creating custom effects > Channel specific filter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 通道專用濾波器
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---


# 通道專用濾波器

效果可以是特定通道的。 在這種情況下，如果你想影響特定通道，你需要建立一個輸入和一個輸出來識別這個通道。 一般來說，輸入/輸出結構應該始終遵守1：1的規則。 如果你想輸入特定頻道，就必須輸出同一個頻道。

濾波器僅影響 **基色** 通道的範例：

![](../../assets/specific-filter-basecolor.png)

>[!NOTE]
>
> 無法將通用設定（輸入/輸出節點）與特定通道（基色/基色）結合。

## Alpha 元件管理

儲存為 RGBA 的通道支援 alpha（例如基色）。 對於這些通道，alpha 輸入/輸出可以直接儲存在 Substance 色彩輸出中。 然而，Substance 引擎不支援灰階影像的 Alpha 版本：必須使用次要地圖來管理。 要取得物質圖中特定通道的 alpha 分量，可以建立一個名為「**channelname\_Alpha**」的灰階輸入，例如： **basecolor\_Alpha**、 **roughness\_Alpha** 等等。\
要輸出這個 alpha 元件，請建立一個與名稱相同的輸出節點。

>[!NOTE]
>
> 每個聲道的特定「**\_Alpha**」輸出在一般 **材質**&#x200B;上無法運作。 要用遮罩隱藏通道，必須建立一個特定的輸出，並採用以下命名慣例：
> 
> * 識別碼： **頻道\_Alpha**
> * 使用情況： **頻道_Alpha**

## 輸入/輸出使用與識別碼列表

>[!NOTE]
>
> 在輸入節點中可以使用 **使用量** 或 **識別碼** （使用權優先權）。

| 頻道名稱 | 使用情況 | 識別碼 / 識別碼 Alpha |
| --- | --- | --- |
| *環境遮蔽* | **環境遮蔽** | **ambientOcclusion / ambientOcclusion\_Alpha** |
| *各向異性角* | **各向異性** | **各向異性角 / 各向異性角\_Alpha** |
| *各向異性能階* | **各向異性** | **各向異性水準 / 各向異性水準\_Alpha** |
| *底色* | **底色** | **baseColor / baseColor\_Alpha** |
| *混合面罩* | **混合遮罩** | **混合遮罩 / 混合遮罩\_Alpha** |
| *彌漫* | **彌漫性** | **擴散/擴散\_Alpha** |
| *遷移* | **遷移** | **位移 / 位移_Alpha** |
| *發射體* | **發射器** | **發射/發射_Alpha** |
| *光澤* | **光澤感** | **光澤 / 光澤_Alpha** |
| *高度* | **高度** | **身高 / 身高\_Alpha** |
| *IOR* | **ior** | **Ior / Ior_Alpha** |
| *金屬* | **金屬感** | **金屬感 / 金屬感\_Alpha** |
| *正常* | **正常** | **正常/正常_Alpha** |
| *不透明度* | **不透明度** | **不透明度 / 不透明度_Alpha** |
| *反思* | **反思** | **反思 / 反思\_Alpha** |
| *粗糙度* | **粗糙度** | **粗糙度 / 粗糙度_Alpha** |
| *散射* | **散射** | **散射 / 散射\_Alpha** |
| *鏡面鏡面* | **鏡面** | **鏡面/鏡面鏡面_Alpha** |
| *鏡面層級* | **高階級** | **specularLevel / specularLevel\_Alpha** |
| *透射式* | **透射式** | **傳遞式 / 傳遞式\_Alpha** |
| *使用者 0* | **使用者0** | **user0 / user0\_Alpha** |
| *使用者 1* | **使用者1** | **用戶1 / 用戶1\_Alpha** |
| *使用者 2* | **使用者2** | **用戶2 / 用戶2\_Alpha** |
| *使用者 3* | **使用者3** | **用戶3 / 用戶3\_Alpha** |
| *使用者 4* | **用戶4** | **用戶4 / 用戶4\_Alpha** |
| *使用者 5* | **用戶5** | **用戶5 / 用戶5\_Alpha** |
| *使用者 6* | **用戶6** | **user6 / user6\_Alpha** |
| *使用者7* | **用戶7** | **用戶7 / 用戶7\_Alpha** |

## 範例

![](../../assets/single-channel.png){width="650px"}

在此範例中，基底色彩的 alpha 通道透過灰階節點擷取，以覆蓋 **粗糙度** 通道。

![](../../assets/mix-channel.png){width="650px"}

在此範例 **中，粗糙度** 通道乘以 **基底色**。
