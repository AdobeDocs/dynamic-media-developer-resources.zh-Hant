---
description: 刪除指定s7 elementID的任何屬性。
seo-description: 刪除指定s7 elementID的任何屬性。
seo-title: deleteAttr
solution: Experience Manager
title: deleteAttr
topic: Scene7 Image Serving - Image Rendering API
uuid: b1176c1a-9ec3-4a95-9f91-97f9f168c252
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# deleteAttr{#deleteattr}

刪除指定s7:elementID的任何屬性。

`deleteAttr.elementID={attributeName%26attributeName}`

如果FXG節點元素已定義， `s7:elementID` 則可使用此命令刪除該節點的屬性。

## 範例 {#section-dece7192384a412c9afdfbda6f08bc97}

`<Group x="130.494" y="102.2246" d:id="4" d:type="layer" d:userLabel="WhiteFrame" visible="true" s7:elementID="middle_area">`

`deleteAttr.middle_area={x%26y%26visible}`

`<Group d:id="4" d:type="layer" d:userLabel="WhiteFrame" s7:elementID="middle_area">`

此示例從原始 *[!DNL x]* FXG節 *[!DNL y]*&#x200B;點中 *[!DNL visible]* 刪除屬性、和。
