---
description: 位址篩選器元素。 <rule>元素中的選用專案。 套用規則時覆寫屬性ClientAddressFilter。
solution: Experience Manager
title: addressfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0da9299b-fe14-4a69-8567-2d79ad2ce0bd
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---

# addressfilter{#addressfilter}

位址篩選器元素。 `<rule>`個元素中的選用專案。 套用規則時覆寫attribute：：ClientAddressFilter。

## 屬性 {#section-e7a0960f7f0045da91de37824aa4aeaa}

無。

## 資料 {#section-eb138f192516418a9ef2ab9a38c9ee9e}

IP位址的逗號分隔清單。 每個個別位址都可包含選用的網路遮罩尾碼，以便指定IP位址範圍。 如需詳細資訊，請參閱[attribute：：ClientAddressFilter](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md)。

## 說明 {#section-099b7839c4be40c68cbff29dad14e7d5}

在`<addressfilter>`元素中指定這些位址，即可限制對此影像目錄的存取權給一或多個特定IP位址。 如果使用者端IP位址不符，則會傳回「已拒絕要求」錯誤給使用者端。

如果`<addressfilter>`為空白或未指定，則不會限制存取。

如果`<rule>`專案中的`<expression>`不存在或空白，則會將`<addressfilter>`套用至所有要求。

`localhost`一律為`ClientAddressFilter`定義的隱含部分，即使未明確指定。 不論`ClientAddressFilter`的規格為何，來自`localhost`的請求都不會被拒絕。

## 另請參閱 {#section-02056065e0c042e1b155b2f3e5b84ef7}

[attribute：：ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
