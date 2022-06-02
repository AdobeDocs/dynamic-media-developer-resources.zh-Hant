---
title: 客戶端地址篩選器
description: 客戶端IP地址篩選器。 允許指定一個或多個IP地址或地址範圍。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 24046950-1dba-4352-a549-43994e799748
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 3%

---

# 客戶端地址篩選器{#clientaddressfilter}

客戶端IP地址篩選器。 允許指定一個或多個IP地址或地址範圍。

如果指定，則拒絕從未列出IP地址的客戶端發出的對此映像目錄的請求。 `localhost` 總是隱式的 `ClientAddressFilter` 定義，即使未明確指定。 源自 `localhost` 不會被拒絕，不管 `ClientAddressFilter` 規範。

## 屬性 {#section-21a2992f108d42fb8660c0d65aa61e13}

IP地址的逗號分隔清單（帶可選網路掩碼）([CIDR表示法](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation) ):

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* IP地址 *[!DNL ddd.ddd.ddd.ddd]* 格式

* *[!DNL netmask]* 網路掩碼(0...32)

當具有 `<addressfilter>` 元素。

## 預設 {#section-beddaa18ed6c4f3ba1eb2d4471267712}

繼承自 `default::AddressFilter` 或為空。

## 範例 {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* 無訪問限制： `0.0.0.0/0`
* 授予對所有地址的訪問權限，以 `192: 192.0.0.0/8`
* 授予對512台主機的訪問權限，其地址介於 `192.168.12.0` 和 `192.168.13.255: 192.168.12.0/23`

* 授予對單個IP地址的訪問權限： `192.168.2.117` 或 `192.168.2.117/32`

## 另請參閱 {#section-6198780c7b3045aabd211eefb38bc565}

[地址篩選器](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
