---
description: 預設的客戶端快取存留時間。 提供預設過期時間間隔，以備特定目錄記錄不包含有效的目錄過期值時使用。
solution: Experience Manager
title: 過期
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: c9dccf8d-56b3-4608-ac05-9c17babc609e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---

# 過期{#expiration}

預設的客戶端快取存留時間。 提供預設過期時間間隔，以備特定目錄記錄不包含有效的目錄：：過期值時使用。

## 屬性 {#section-063be3b2f13a48a3a5ab8080718e9812}

實數，0或更高。 自回覆資料產生以來直到到期的小時數。 設為0一律會立即讓回覆影像過期，這會有效停用用戶端快取。 設為–1以標示為`never expire`。

## 預設 {#section-f55308b195c04083996f6717c8537634}

如果未定義或為空，則從`default::Expiration`繼承。

TTL（存留時間）是快取過期前的持續時間。 預設TTL為10小時。

## 另請參閱 {#section-b2411d99ddb14115ad475d506efd8967}

[目錄：:Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ，屬 [性：:DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)，屬 [性：:NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
