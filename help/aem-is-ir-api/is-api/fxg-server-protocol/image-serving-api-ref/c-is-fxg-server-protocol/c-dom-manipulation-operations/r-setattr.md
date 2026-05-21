---
title: setAttr
description: 設定指定s7 elementID的任何屬性。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
TQID: 'https://experienceleague.adobe.com/0O1uOLXsh-5PkBnXugpQYJHDAZep49WO3AA4hjClODk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 98
ht-degree: 1%

---

# setAttr{#setattr}

設定指定s7:elementID的任何屬性。

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

如果FXG節點元素已定義`s7:elementID`，您可以操作該節點的屬性。 您可以視需要設定多個屬性/值組。 屬性不需要在FXG中定義，但是它必須對節點元素有效。 所有介於`{}`之間的值都必須逸出。

## 範例 {#section-9c37470d5f0349e5b0a97291782cb7a6}

假設已為`BitmapGraphic`節點定義`s7:elementID="Group1"`屬性，則下列為有效：

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

此範例會設定`BitmapGraphic`的&#x200B;*[!DNL x]*、*[!DNL y]*、*[!DNL rotation]*、*[!DNL scaleX]*&#x200B;和&#x200B;*[!DNL scaleY]*，並覆寫任何現有的值。
