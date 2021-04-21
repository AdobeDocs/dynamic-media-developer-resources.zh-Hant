---
description: 預設的用戶端快取上線時間。 提供預設的過期間隔，以防特定目錄記錄不包含有效的目錄過期或暈映過期值，或是直接存取暈映檔案或材質檔案，而非透過目錄記錄。
solution: Experience Manager
title: 過期
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 3%

---


# 過期{#expiration}

預設的用戶端快取上線時間。 提供預設的過期間隔，以防特定目錄記錄不包含有效目錄：：過期或暈映：：過期值，或直接存取暈映檔案或材質檔案，而非透過目錄記錄。

## 屬性 {#section-8e2bade105ec4905ae5c4911f500279f}

實數，0或更大。 自回覆資料產生以來，到期前的小時數。 設為0，一律會立即使回覆影像過期，這會有效停用用戶端快取。 設為-1，標示為&#x200B;*永不過期*。

## 預設 {#section-18cfce46edb441bfae7dd9d3e0217ba9}

繼承自預設值：：如果未定義或為空，則為過期。

## 另請參閱 {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[目錄：：過期](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) ，暈 [映：：過期](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
