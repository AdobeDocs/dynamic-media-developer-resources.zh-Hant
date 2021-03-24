---
description: 地址篩選元素。 在<rule>元素中為可選項。 在套用規則時覆寫屬性ClientAddressFilter。
solution: Experience Manager
title: 地址篩選
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 4%

---


# 地址篩選器{#addressfilter}

地址篩選元素。 在`<rule>`元素中為可選項。 覆寫屬性：：套用規則時的ClientAddressFilter。

## 屬性 {#section-e7a0960f7f0045da91de37824aa4aeaa}

無。

## 資料 {#section-eb138f192516418a9ef2ab9a38c9ee9e}

IP位址的逗號分隔清單。 每個單獨地址可包括可選網路掩碼尾碼以允許指定IP地址範圍。 如需詳細資訊，請參閱` [attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)`。

## 說明 {#section-099b7839c4be40c68cbff29dad14e7d5}

在`<addressfilter>`元素中指定此影像目錄的存取權可限制為一個或多個特定IP位址。 如果客戶端IP位址不相符，則會傳回「請求拒絕」錯誤給客戶端。

如果`<addressfilter>`為空或未指定，則不限制訪問。

如果`<rule>`元素中的`<expression>`不存在或為空，則`<addressfilter>`將應用於所有請求。

`localhost` 一律是定義的隱 `ClientAddressFilter` 式部分，即使未明確指定。不論`ClientAddressFilter`規格為何，始自`localhost`的請求一律不會遭拒。

## 請參閱{#section-02056065e0c042e1b155b2f3e5b84ef7}

[屬性：:ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
