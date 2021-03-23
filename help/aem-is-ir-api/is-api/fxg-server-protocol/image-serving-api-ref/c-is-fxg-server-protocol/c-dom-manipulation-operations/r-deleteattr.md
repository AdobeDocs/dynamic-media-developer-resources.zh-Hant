---
description: 刪除指定s7 elementID的任何屬性。
seo-description: 刪除指定s7 elementID的任何屬性。
seo-title: deleteAttr
solution: Experience Manager
title: deleteAttr
uuid: b1176c1a-9ec3-4a95-9f91-97f9f168c252
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 1%

---


# deleteAttr{#deleteattr}

刪除指定s7:elementID的任何屬性。

`deleteAttr.elementID={attributeName%26attributeName}`

如果FXG節點元素已定義`s7:elementID`，則可使用此命令刪除該節點的屬性。

## 範例 {#section-dece7192384a412c9afdfbda6f08bc97}

`<Group x="130.494" y="102.2246" d:id="4" d:type="layer" d:userLabel="WhiteFrame" visible="true" s7:elementID="middle_area">`

`deleteAttr.middle_area={x%26y%26visible}`

`<Group d:id="4" d:type="layer" d:userLabel="WhiteFrame" s7:elementID="middle_area">`

此示例從原始FXG節點中刪除&#x200B;*[!DNL x]*、*[!DNL y]*&#x200B;和&#x200B;*[!DNL visible]*&#x200B;屬性。
