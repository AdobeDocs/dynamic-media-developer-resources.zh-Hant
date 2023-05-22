---
description: 為s7 elementID設定文本節點值。
solution: Experience Manager
title: 設定值
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 1%

---

# 設定值{#setval}

為s7:elementID設定文本節點值。

`setVal.elementID= *[!DNL value]*`

如果FXG節點元素具有 `s7:elementID` 定義，可以處理該節點的文本值。

## 範例 {#section-f574fd66dedd4a219aa537d7bdabea23}

假設 `s7:elementID="paragraph1"` 為 `TextGraphic` 節點，則以下內容有效：

`&setVal.paragraph=Hello`

此示例將段落節點的文本值設定為「Hello」。
