---
description: 預設的用戶端快取上線時間。 提供預設的過期間隔，以防特定目錄記錄不包含有效的目錄過期值。
solution: Experience Manager
title: 過期
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 4%

---


# 過期{#expiration}

預設的用戶端快取上線時間。 提供預設的過期間隔，以防特定目錄記錄不包含有效的目錄：：過期值。

## 屬性 {#section-063be3b2f13a48a3a5ab8080718e9812}

實數，0或更大。 自回覆資料產生以來，到期前的小時數。 設為0，一律會立即使回覆影像過期，這會有效停用用戶端快取。 設定為-1以標籤為`never expire`。

## 預設 {#section-f55308b195c04083996f6717c8537634}

如果未定義或為空，則繼承自`default::Expiration`。

TTL（存留時間）是快取過期前的持續時間。 預設TTL為10小時。

## 另請參閱 {#section-b2411d99ddb14115ad475d506efd8967}

[catalog:::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [attribute::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf),  [attribute::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
