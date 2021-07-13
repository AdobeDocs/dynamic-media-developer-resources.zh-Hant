---
description: 為指定的s7 elementID設定任何屬性。
solution: Experience Manager
title: setAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# setAttr{#setattr}

為指定的s7:elementID設定任何屬性。

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

如果FXG節點元素已定義`s7:elementID`，則可以操作該節點的屬性。 您可以視需要設定任意數量的屬性/值組。 屬性不需要在FXG中定義，但對於節點元素必須有效。 `{}`之間的所有值都必須逸出。

## 範例 {#section-9c37470d5f0349e5b0a97291782cb7a6}

假設已為`BitmapGraphic`節點定義`s7:elementID="Group1"`屬性，則以下內容有效：

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

此示例為`BitmapGraphic`設定&#x200B;*[!DNL x]*、*[!DNL y]*、*[!DNL rotation]*、*[!DNL scaleX]*&#x200B;和&#x200B;*[!DNL scaleY]*，並覆蓋任何現有值。
