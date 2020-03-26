---
description: 用戶端IP位址篩選。 允許指定一個或多個IP地址或地址範圍。
seo-description: 用戶端IP位址篩選。 允許指定一個或多個IP地址或地址範圍。
seo-title: ClientAddressFilter
solution: Experience Manager
title: ClientAddressFilter
topic: Scene7 Image Serving - Image Rendering API
uuid: b68f527b-7fa7-43e3-9517-57a6c3700b06
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# ClientAddressFilter{#clientaddressfilter}

用戶端IP位址篩選。 允許指定一個或多個IP地址或地址範圍。

指定時，會拒絕從未列出IP位址的客戶端發出的對此映像目錄的請求。 `localhost` 一律是定義的隱 `ClientAddressFilter` 式部分，即使未明確指定。 不論規格 `localhost` 為何，始發請求一律不 `ClientAddressFilter` 予拒絕。

## 屬性 {#section-21a2992f108d42fb8660c0d65aa61e13}

IP位址的逗號分隔清單(使用[CIDR符號](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation) ):

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* 格式化的IP位 *[!DNL ddd.ddd.ddd.ddd]* 址

* *[!DNL netmask]* 淨掩碼(0...32)

套用含元素的預處理規則時，會忽略 `<addressfilter>` 此屬性。

## 預設 {#section-beddaa18ed6c4f3ba1eb2d4471267712}

繼承自 `default::AddressFilter` （如果未定義或為空）。

## 範例 {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* 無存取限制： `0.0.0.0/0`
* 授予所有地址的訪問權限，從 `192: 192.0.0.0/8`
* 授予對512台主機的訪問權限，其地址介於 `192.168.12.0` 和 `192.168.13.255: 192.168.12.0/23`

* 授予對單個IP地址的訪問權： `192.168.2.117` 或 `192.168.2.117/32`

## 另請參閱 {#section-6198780c7b3045aabd211eefb38bc565}

[地址篩選](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
