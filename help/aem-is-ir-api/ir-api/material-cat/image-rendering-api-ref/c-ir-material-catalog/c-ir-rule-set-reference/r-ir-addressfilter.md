---
description: 地址篩選元素。 在<rule>元素中為選用。 套用規則時覆寫屬性ClientAddressFilter。
solution: Experience Manager
title: 地址篩選器
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0da9299b-fe14-4a69-8567-2d79ad2ce0bd
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 4%

---

# 地址篩選器{#addressfilter}

地址篩選元素。 `<rule>`元素中為可選。 套用規則時覆寫屬性：:ClientAddressFilter。

## 屬性 {#section-e7a0960f7f0045da91de37824aa4aeaa}

無。

## 資料 {#section-eb138f192516418a9ef2ab9a38c9ee9e}

IP位址清單（以逗號分隔）。 每個單個地址可以包括可選的網路掩碼尾碼，以允許指定IP地址範圍。 如需詳細資訊，請參閱` [attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)`。

## 說明 {#section-099b7839c4be40c68cbff29dad14e7d5}

通過在`<addressfilter>`元素中指定此映像目錄，可以限制對一個或多個特定IP地址的訪問。 如果客戶端IP地址不匹配，則返回「拒絕請求」錯誤。

如果`<addressfilter>`為空或未指定，則不限制訪問。

如果`<rule>`元素中的`<expression>`不存在或為空，則`<addressfilter>`會套用至所有請求。

`localhost` 一律會隱含在定義中，即 `ClientAddressFilter` 使未明確指定亦然。無論`ClientAddressFilter`規格為何，源自`localhost`的請求從不被拒絕。

## SeeaAlso {#section-02056065e0c042e1b155b2f3e5b84ef7}

[屬性：:ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
