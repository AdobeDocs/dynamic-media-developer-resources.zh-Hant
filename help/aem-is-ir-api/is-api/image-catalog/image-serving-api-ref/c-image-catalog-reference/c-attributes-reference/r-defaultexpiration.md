---
description: 預設影像回應的用戶端快取TTL。 提供預設影像回應的過期時間間隔（傳回以defaultImage=或屬性DefaultImage指定的預設影像的回應）。
solution: Experience Manager
title: DefaultExpiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 99103681-c00c-4648-8dee-2314e7e614af
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 2%

---

# DefaultExpiration{#defaultexpiration}

預設影像回應的用戶端快取TTL。 提供預設影像回應的過期時間間隔（傳回以defaultImage=或attribute::DefaultImage指定的預設影像的回應）。

僅當預設影像未與目錄記錄相關聯，或預設影像目錄記錄未提供特定`catalog::Expiration`值時，才應用。

## 屬性 {#section-e564512476604fd7b964f9f2903d6d33}

實數，0或更高。 自回覆資料產生以來直到到期的小時數。 設為0一律會立即讓回覆影像過期，如此可有效停用預設影像回應的用戶端快取。 設為`-1`以標示為`never expire`。

## 預設 {#section-131cd32c2e214391857dba5af321f8cd}

如果未定義或為空，則從`default::DefaultExpiration`繼承。

TTL（存留時間）是快取過期前的持續時間。 預設TTL為1小時。

## 另請參閱 {#section-d8642c22e3d947129367dd76366963d6}

[目錄：:Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [屬性：:DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
