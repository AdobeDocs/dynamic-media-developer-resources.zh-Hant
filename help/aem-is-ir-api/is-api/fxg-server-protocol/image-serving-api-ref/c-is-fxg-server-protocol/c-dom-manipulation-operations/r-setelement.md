---
description: 將XML設為s7 elementID。
seo-description: 將XML設為s7 elementID。
seo-title: setElement
solution: Experience Manager
title: setElement
topic: Scene7 Image Serving - Image Rendering API
uuid: 717c9c3c-a2e0-4179-8158-9913f4e09a96
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setElement{#setelement}

將XML設為s7:elementID。

`setElement.elementID=<XML>`

如果FXG節點元素已定義， `s7:elementID` 則值將 `<XML>` 被替換為子元素。 The `<XML>` must be encoded.

## 範例 {#section-f23a998b18994dd3b5d4e1965718db9f}

假設已 `s7:elementID="group2"` 為節點定義屬性， `Group` 則下列內容有效：

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

此示例從節點中刪除所有子 `group2`節點，並用新子節點 `TextGraphic` 替換它。
