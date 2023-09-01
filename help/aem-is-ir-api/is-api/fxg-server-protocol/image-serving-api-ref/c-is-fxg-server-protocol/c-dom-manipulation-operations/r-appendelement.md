---
title: appendElement
description: 將XML附加至s7 elementID。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f93bc31e-c0ae-4375-bb6a-eba6f11945b2
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 1%

---

# appendElement{#appendelement}

將XML附加至s7：elementID。

`appendElement.elementID=<XML>`

如果FXG節點元素具有 `s7:elementID` 已定義， `<XML>` 值會附加為子元素。 此 `<XML>` 必須編碼。

## 範例 {#section-4368570aa198485d91b73b4d0741478f}

假設 `s7:elementID="group1"` 屬性是為「群組」節點定義的，則下列專案有效：

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

此範例會將文字圖形子系附加至 `group1`.
