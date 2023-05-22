---
description: 預設客戶端快取的生存時間。 在特定目錄記錄不包含有效的目錄到期值時提供預設到期間隔。
solution: Experience Manager
title: 過期
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c9dccf8d-56b3-4608-ac05-9c17babc609e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 4%

---

# 過期{#expiration}

預設客戶端快取的生存時間。 如果特定目錄記錄不包含有效的目錄：:Expiration值，則提供預設的過期間隔。

## 屬性 {#section-063be3b2f13a48a3a5ab8080718e9812}

實數，0或更大。 自生成回復資料以來到期的小時數。 設定為0時，始終立即使回復映像過期，這將有效地禁用客戶端快取。 設定為–1以標籤為 `never expire`。

## 預設 {#section-f55308b195c04083996f6717c8537634}

繼承自 `default::Expiration` 或為空。

TTL(Time-To-Live)是快取過期前的持續時間。 預設TTL為10小時。

## 另請參閱 {#section-b2411d99ddb14115ad475d506efd8967}

[目錄：：到期](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) 。 [屬性：:DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)。 [屬性：:NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
