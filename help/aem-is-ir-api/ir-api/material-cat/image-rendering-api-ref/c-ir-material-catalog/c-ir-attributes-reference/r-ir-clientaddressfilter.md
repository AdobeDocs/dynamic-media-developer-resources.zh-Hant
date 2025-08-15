---
title: ClientAddressfilter
description: 使用者端IP位址篩選器。 允許指定一個或多個IP位址或位址範圍。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 24046950-1dba-4352-a549-43994e799748
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---

# ClientAddressfilter{#clientaddressfilter}

使用者端IP位址篩選器。 允許指定一個或多個IP位址或位址範圍。

指定後，系統會拒絕從未列出的IP位址之使用者端對此影像目錄提出的要求。 `localhost`一律為`ClientAddressFilter`定義的隱含部分，即使未明確指定。 不論`localhost`的規格為何，來自`ClientAddressFilter`的請求都不會被拒絕。

## 屬性 {#section-21a2992f108d42fb8660c0d65aa61e13}

以逗號分隔的IP位址清單，含選擇性的Netmask （使用[CIDR標籤法](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation)）：

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]*&#x200B;格式的&#x200B;*[!DNL ddd.ddd.ddd.ddd]* IP位址

* *[!DNL netmask]*&#x200B;網路遮罩（0到32）

當套用含`<addressfilter>`元素的預先處理規則時，會忽略此屬性。

## 預設 {#section-beddaa18ed6c4f3ba1eb2d4471267712}

如果未定義或空白，則繼承自`default::AddressFilter`。

## 範例 {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* 無存取限制： `0.0.0.0/0`
* 授與以`192: 192.0.0.0/8`開頭的所有位址的存取權
* 授與存取許可權給位址介於`192.168.12.0`到`192.168.13.255: 192.168.12.0/23`之間的512部主機

* 授與單一IP位址的存取權： `192.168.2.117`或`192.168.2.117/32`

## 另請參閱 {#section-6198780c7b3045aabd211eefb38bc565}

[addressfilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
