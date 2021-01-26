---
description: 為s7 elementID設定文位元組點值。
seo-description: 為s7 elementID設定文位元組點值。
seo-title: setVal
solution: Experience Manager
title: setVal
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 27ced070-6434-477d-aacf-053d53ee58ff
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
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
