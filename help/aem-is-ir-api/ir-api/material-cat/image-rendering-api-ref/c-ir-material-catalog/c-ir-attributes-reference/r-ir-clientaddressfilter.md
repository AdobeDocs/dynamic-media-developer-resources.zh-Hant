---
title: ClientAddressfilter
description: 使用者端IP位址篩選器。 允許指定一個或多個IP位址或位址範圍。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 24046950-1dba-4352-a549-43994e799748
TQID: 'https://experienceleague.adobe.com/azMITpRcITTOEB0FCev6vWiTmocumP-0HTQD3rIV-fA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 156
ht-degree: 2%

---

# ClientAddressfilter{#clientaddressfilter}

使用者端IP位址篩選器。 允許指定一個或多個IP位址或位址範圍。

指定後，系統會拒絕從未列出的IP位址之使用者端對此影像目錄提出的要求。 `localhost`一律為`ClientAddressFilter`定義的隱含部分，即使未明確指定。 不論`ClientAddressFilter`的規格為何，來自`localhost`的請求都不會被拒絕。

## 屬性 {#section-21a2992f108d42fb8660c0d65aa61e13}

以逗號分隔的IP位址清單，含選擇性的Netmask （使用[CIDR標籤法](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation)）：

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ddd.ddd.ddd.ddd]*&#x200B;格式的&#x200B;*[!DNL ipAddress]* IP位址

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

