---
description: 刪除指定s7 elementID的任何屬性。
solution: Experience Manager
title: deleteAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7cecd0aa-c928-4652-a92f-f21ebcf83304
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 1%

---

# deleteAttr{#deleteattr}

刪除指定s7:elementID的任何屬性。

`deleteAttr.elementID={attributeName%26attributeName}`

如果FXG節點元素已定義`s7:elementID`，則可以使用此命令刪除該節點的屬性。

## 範例 {#section-dece7192384a412c9afdfbda6f08bc97}

`<Group x="130.494" y="102.2246" d:id="4" d:type="layer" d:userLabel="WhiteFrame" visible="true" s7:elementID="middle_area">`

`deleteAttr.middle_area={x%26y%26visible}`

`<Group d:id="4" d:type="layer" d:userLabel="WhiteFrame" s7:elementID="middle_area">`

此示例從原始FXG節點中刪除屬性&#x200B;*[!DNL x]*、*[!DNL y]*&#x200B;和&#x200B;*[!DNL visible]*。
