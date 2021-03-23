---
description: 用戶端快取TTL，以取得預設影像回應。 提供預設影像回應的過期時間間隔（傳回以defaultImage=或屬性DefaultImage指定之預設影像的回應）。
seo-description: 用戶端快取TTL，以取得預設影像回應。 提供預設影像回應的過期時間間隔（傳回以defaultImage=或屬性DefaultImage指定之預設影像的回應）。
seo-title: DefaultExpiration
solution: Experience Manager
title: DefaultExpiration
uuid: 5266bff9-f20b-4b3b-9566-8a3f5ba0777a
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 2%

---


# DefaultExpiration{#defaultexpiration}

用戶端快取TTL，以取得預設影像回應。 提供預設影像回應的過期時間間隔（傳回以defaultImage=或attribute::DefaultImage指定之預設影像的回應）。

僅當預設影像與目錄記錄無關或預設影像目錄記錄未提供特定`catalog::Expiration`值時才應用。

## 屬性 {#section-e564512476604fd7b964f9f2903d6d33}

實數，0或更大。 自回覆資料產生以來，到期前的小時數。 設為0，一律立即使回覆影像過期，這會有效停用用戶端快取預設影像回應。 設為`-1`以標示為`never expire`。

## 預設 {#section-131cd32c2e214391857dba5af321f8cd}

如果未定義或為空，則繼承自`default::DefaultExpiration`。

TTL（存留時間）是快取過期前的持續時間。 預設TTL為1小時。

## 另請參閱 {#section-d8642c22e3d947129367dd76366963d6}

[目錄：:Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ，屬 [性：:DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
