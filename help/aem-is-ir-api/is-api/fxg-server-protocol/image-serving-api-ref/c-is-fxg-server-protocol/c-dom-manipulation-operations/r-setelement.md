---
description: 將XML設為s7 elementID。
solution: Experience Manager
title: setElement
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 1%

---


# setElement{#setelement}

將XML設為s7:elementID。

`setElement.elementID=<XML>`

如果FXG節點元素已定義`s7:elementID`，則`<XML>`值將被替換為子元素。 `<XML>`必須進行編碼。

## 範例 {#section-f23a998b18994dd3b5d4e1965718db9f}

假設為`Group`節點定義了`s7:elementID="group2"`屬性，則以下屬性有效：

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

此示例從`group2`節點中刪除所有子節點，並用新的`TextGraphic`子節點替換該子節點。
