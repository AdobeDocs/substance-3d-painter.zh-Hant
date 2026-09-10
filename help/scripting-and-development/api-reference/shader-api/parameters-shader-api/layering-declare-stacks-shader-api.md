---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/scripting-and-development/api-reference/shader-api/parameters-shader-api/layering-declare-stacks-shader-api.html"
breadcrumb-title: ''
description: 存取 Substance 3D Painter 的 Layering Declare Stacks shader API 參考，以建立自訂材質分層堆疊。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API > Parameters - Shader API > Layering Declare Stacks - Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Layering 宣告堆疊 - Shader API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# Layering 宣告堆疊 - Shader API

## 材質分層：宣告可編輯堆疊

可編輯堆疊由唯一識別碼及文件通道列表定義。 可能的通道識別碼包括：*環境遮蔽、**各向異性、**&#x200B;各向異性、各向異性、**底色**&#x200B;混合遮罩&#x200B;**、漫反射**&#x200B;**、發光**&#x200B;**光度、高度**&#x200B;**或金屬**、正常&#x200B;**不透明度**、**反射、粗糙度**、**散射、鏡**&#x200B;面級&#x200B;**透射。* user0 使用者1 &#x200B;** user2 user3 **&#x200B; ** user4 **&#x200B; user5 &#x200B;** user6 **&#x200B; user7 &#x200B;**&#x200B;**

範例：

```
//:  stacks [ 

//:    { 

//:      "id": "Mask1", 

//:      "channels": [ 

//:        {"id": "opacity"} 

//:      ] 

//:    }, { 

//:      "id": "Mask2", 

//:      "channels": [ 

//:        {"id": "opacity"}, 

//:        {"id": "user0"} 

//:      ] 

//:    } 

//:  ]
```


要將堆疊通道綁定到取樣器參數，請在通道標籤前加上堆疊識別碼：

```
//: param auto Mask1.channel_opacity 

uniform sampler2D mask_tex1; 

//: param auto Mask2.channel_opacity 

uniform sampler2D mask_tex2; 

 
```
