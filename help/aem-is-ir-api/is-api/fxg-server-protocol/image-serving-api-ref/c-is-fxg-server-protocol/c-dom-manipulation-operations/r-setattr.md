---
description: 設定指定s7 elementID的任何屬性。
seo-description: 設定指定s7 elementID的任何屬性。
seo-title: setAttr
solution: Experience Manager
title: setAttr
uuid: 968f7496-3cd4-4670-96fc-53127bba9a83
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---


# setAttr{#setattr}

設定指定s7:elementID的任何屬性。

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

如果FXG節點元素已定義`s7:elementID`，則可以操作該節點的屬性。 您可以視需要設定任意數量的屬性／值對。 屬性不必已在FXG中定義，但對節點元素必須有效。 `{}`之間的所有值都必須「逸出」。

## 範例 {#section-9c37470d5f0349e5b0a97291782cb7a6}

假設為`BitmapGraphic`節點定義了`s7:elementID="Group1"`屬性，則以下是有效的：

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

此示例為`BitmapGraphic`設定&#x200B;*[!DNL x]*、*[!DNL y]*、*[!DNL rotation]*、*[!DNL scaleX]*&#x200B;和&#x200B;*[!DNL scaleY]*，並覆蓋所有現有值。
