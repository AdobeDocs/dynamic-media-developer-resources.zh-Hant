---
title: setAttr
description: 設定指定s7 elementID的任何屬性。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 1%

---

# setAttr{#setattr}

設定指定s7:elementID的任何屬性。

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

如果FXG節點元素已定義`s7:elementID`，您可以操作該節點的屬性。 您可以視需要設定多個屬性/值組。 屬性不需要在FXG中定義，但是它必須對節點元素有效。 所有介於`{}`之間的值都必須逸出。

## 範例 {#section-9c37470d5f0349e5b0a97291782cb7a6}

假設已為`s7:elementID="Group1"`節點定義`BitmapGraphic`屬性，則下列為有效：

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

此範例會設定&#x200B;*[!DNL x]*&#x200B;的&#x200B;*[!DNL y]*、*[!DNL rotation]*、*[!DNL scaleX]*、*[!DNL scaleY]*&#x200B;和`BitmapGraphic`，並覆寫任何現有的值。
