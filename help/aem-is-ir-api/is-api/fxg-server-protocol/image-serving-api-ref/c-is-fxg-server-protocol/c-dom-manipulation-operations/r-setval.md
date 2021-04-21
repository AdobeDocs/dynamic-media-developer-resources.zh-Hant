---
description: 為s7 elementID設定文位元組點值。
solution: Experience Manager
title: setVal
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 1%

---


# setVal{#setval}

為s7:elementID設定文位元組點值。

`setVal.elementID= *[!DNL value]*`

如果FXG節點元素已定義`s7:elementID`，則可操作該節點的文本值。

## 範例 {#section-f574fd66dedd4a219aa537d7bdabea23}

假設為`TextGraphic`節點定義了`s7:elementID="paragraph1"`屬性，則以下屬性有效：

`&setVal.paragraph=Hello`

此示例將段落節點的文本值設定為&quot;Hello&quot;。
