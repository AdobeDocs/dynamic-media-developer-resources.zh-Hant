---
description: 非影像回應的使用者端快取TTL。 提供某些非影像回應的到期時間間隔。
solution: Experience Manager
title: NonImgExpiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c61e2781-dfaa-4f3d-958d-5ffa755a3e4d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 2%

---

# NonImgExpiration{#nonimgexpiration}

非影像回應的使用者端快取TTL。 提供某些非影像回應的到期時間間隔。

提供某些非影像回應的到期時間間隔，包括回應下列命令所傳送的回應：

* `req=imageset`
* `req=catalogprops`
* `req=exists`
* `req=imageprops`
* `req=props`

## 屬性 {#section-d37e3113f4b1468b86b5a14e80d94c83}

實數，0或更大。 從產生回覆資料到到期為止的小時數。 設為0可一律使回覆影像立即過期，這會有效停用預設影像回應的使用者端快取。 設為–1以標籤為&#x200B;*永不過期*。

## 預設 {#section-96981360c0234b7f824d2ff7c25a7954}

如果未定義或空白，則繼承自`default::NonImgExpiration`。

TTL （存留時間）是快取過期前的持續時間。 預設TTL為6分鐘。

## 另請參閱 {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[目錄：：Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ， [屬性：：DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
