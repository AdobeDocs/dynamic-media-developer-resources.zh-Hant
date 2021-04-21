---
description: 將XML附加至s7 elementID。
solution: Experience Manager
title: appendElement
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 1%

---


# appendElement{#appendelement}

將XML附加至s7:elementID。

`appendElement.elementID=<XML>`

如果FXG節點元素已定義`s7:elementID`，則`<XML>`值會附加為子元素。 `<XML>`必須進行編碼。

## 範例 {#section-4368570aa198485d91b73b4d0741478f}

假設已為組節點定義了`s7:elementID="group1"`屬性，則以下屬性有效：

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

此示例將文本圖形子項附加到`group1`。
