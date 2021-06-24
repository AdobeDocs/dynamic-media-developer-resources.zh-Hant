---
description: 客戶端IP地址篩選器。 允許規範一個或多個IP地址或地址範圍。
solution: Experience Manager
title: ClientAddressFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 24046950-1dba-4352-a549-43994e799748
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 3%

---

# ClientAddressFilter{#clientaddressfilter}

客戶端IP地址篩選器。 允許規範一個或多個IP地址或地址範圍。

指定後，對此映像目錄的請求將被拒絕，這些請求源自於位於未列出IP地址的客戶端。 `localhost` 一律會隱含在定義中，即 `ClientAddressFilter` 使未明確指定亦然。無論`ClientAddressFilter`規格為何，源自`localhost`的請求從不被拒絕。

## 屬性 {#section-21a2992f108d42fb8660c0d65aa61e13}

以逗號分隔的IP位址清單，並搭配選用的網路掩碼（使用[CIDR標籤法](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation)）:

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* 格式的IP位 *[!DNL ddd.ddd.ddd.ddd]* 址

* *[!DNL netmask]* 淨掩碼(0...32)

套用具有`<addressfilter>`元素的預先處理規則時，會忽略此屬性。

## 預設 {#section-beddaa18ed6c4f3ba1eb2d4471267712}

如果未定義或為空，則從`default::AddressFilter`繼承。

## 範例 {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* 無訪問限制：`0.0.0.0/0`
* 授予對以`192: 192.0.0.0/8`開頭的所有地址的訪問權
* 授予對地址介於`192.168.12.0`和`192.168.13.255: 192.168.12.0/23`之間的512台主機的訪問權

* 授予對單一IP位址的存取權：`192.168.2.117`或`192.168.2.117/32`

## 另請參閱 {#section-6198780c7b3045aabd211eefb38bc565}

[地址篩選器](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
