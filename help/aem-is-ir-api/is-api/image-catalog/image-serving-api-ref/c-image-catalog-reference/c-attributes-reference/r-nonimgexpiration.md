---
description: 非影像回應的用戶端快取TTL。 提供某些非影像回應的過期間隔。
seo-description: 非影像回應的用戶端快取TTL。 提供某些非影像回應的過期間隔。
seo-title: NonImgExpiration
solution: Experience Manager
title: NonImgExpiration
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 19b37bd4-f7cf-4b5f-be1a-b2d9fda5b4b1
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---


# NonImgExpiration{#nonimgexpiration}

非影像回應的用戶端快取TTL。 提供某些非影像回應的過期間隔。

提供某些非映像響應的過期間隔，包括響應以下命令而發送的響應：

* `req=imageset`
* `req=catalogprops`
* `req=exists`
* `req=imageprops`
* `req=props`

## 屬性 {#section-d37e3113f4b1468b86b5a14e80d94c83}

實數，0或更大。 自回覆資料產生以來，到期前的小時數。 設為0，一律立即使回覆影像過期，這會有效停用用戶端快取預設影像回應。 設為-1，標示為&#x200B;*永不過期*。

## 預設 {#section-96981360c0234b7f824d2ff7c25a7954}

如果未定義或為空，則繼承自`default::NonImgExpiration`。

TTL（存留時間）是快取過期前的持續時間。 預設TTL為6分鐘。

## 另請參閱 {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[目錄：:Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ，屬 [性：:DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
