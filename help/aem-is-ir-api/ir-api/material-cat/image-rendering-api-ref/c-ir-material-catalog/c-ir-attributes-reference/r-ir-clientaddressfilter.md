---
description: 用戶端IP位址篩選。 允許指定一個或多個IP地址或地址範圍。
solution: Experience Manager
title: ClientAddressFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 3%

---


# ClientAddressFilter{#clientaddressfilter}

用戶端IP位址篩選。 允許指定一個或多個IP地址或地址範圍。

指定時，會拒絕從未列出IP位址的客戶端發出的對此映像目錄的請求。 `localhost` 一律是定義的隱 `ClientAddressFilter` 式部分，即使未明確指定。不論`ClientAddressFilter`規格為何，始自`localhost`的請求一律不會遭拒。

## 屬性 {#section-21a2992f108d42fb8660c0d65aa61e13}

IP地址的逗號分隔清單(使用可選網路掩碼（[CIDR符號](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation)）:

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* 格式化的IP位 *[!DNL ddd.ddd.ddd.ddd]* 址

* *[!DNL netmask]* 淨掩碼(0...32)

套用含`<addressfilter>`元素的預處理規則時，會忽略此屬性。

## 預設 {#section-beddaa18ed6c4f3ba1eb2d4471267712}

如果未定義或為空，則繼承自`default::AddressFilter`。

## 範例 {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* 無存取限制：`0.0.0.0/0`
* 授予對所有地址的訪問權限，從`192: 192.0.0.0/8`開始
* 授予對地址介於`192.168.12.0`和`192.168.13.255: 192.168.12.0/23`之間的512台主機的訪問權

* 授予對單個IP地址的訪問權：`192.168.2.117`或`192.168.2.117/32`

## 另請參閱 {#section-6198780c7b3045aabd211eefb38bc565}

[地址篩選](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
