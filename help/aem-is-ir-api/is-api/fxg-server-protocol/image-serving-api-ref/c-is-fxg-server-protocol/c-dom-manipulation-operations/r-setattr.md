---
description: 為給定s7 elementID設定任何屬性。
solution: Experience Manager
title: setAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 1%

---

# setAttr{#setattr}

為給定s7:elementID設定任何屬性。

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

如果FXG節點元素具有 `s7:elementID` 定義後，可以處理該節點的屬性。 可以根據需要設定任意數量的屬性/值對。 屬性不必已在FXG中定義，但必須對節點元素有效。 介於 `{}` 必須是逃出的。

## 範例 {#section-9c37470d5f0349e5b0a97291782cb7a6}

假設 `s7:elementID="Group1"` 為 `BitmapGraphic` ，則下面的內容有效：

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

此示例設定 *[!DNL x]*。 *[!DNL y]*。 *[!DNL rotation]*。 *[!DNL scaleX]*, *[!DNL scaleY]* 為 `BitmapGraphic` 並覆蓋任何現有值。
