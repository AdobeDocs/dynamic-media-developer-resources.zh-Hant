---
description: 將XML設為s7 elementID。
solution: Experience Manager
title: setElement
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 979e6070-6e24-4caf-9d87-2c80b734c996
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 1%

---

# setElement{#setelement}

將XML設為s7:elementID。

`setElement.elementID=<XML>`

如果FXG節點元素已定義`s7:elementID`，則`<XML>`值將被替換為子元素。 必須對`<XML>`進行編碼。

## 範例 {#section-f23a998b18994dd3b5d4e1965718db9f}

假設已為`Group`節點定義`s7:elementID="group2"`屬性，則下列內容有效：

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

此示例從`group2`節點中刪除所有子節點，並將其替換為新的`TextGraphic`子節點。
