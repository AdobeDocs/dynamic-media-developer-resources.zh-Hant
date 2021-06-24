---
description: 非影像回應的用戶端快取TTL。 提供某些非影像回應的過期時間間隔。
solution: Experience Manager
title: NonImgExpiration
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: c61e2781-dfaa-4f3d-958d-5ffa755a3e4d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 3%

---

# NonImgExpiration{#nonimgexpiration}

非影像回應的用戶端快取TTL。 提供某些非影像回應的過期時間間隔。

提供某些非影像響應的過期時間間隔，包括響應以下命令發送的響應：

* `req=imageset`
* `req=catalogprops`
* `req=exists`
* `req=imageprops`
* `req=props`

## 屬性 {#section-d37e3113f4b1468b86b5a14e80d94c83}

實數，0或更高。 自回覆資料產生以來直到到期的小時數。 設為0一律會立即讓回覆影像過期，如此可有效停用預設影像回應的用戶端快取。 設為–1以標示為&#x200B;*永不過期*。

## 預設 {#section-96981360c0234b7f824d2ff7c25a7954}

如果未定義或為空，則從`default::NonImgExpiration`繼承。

TTL（存留時間）是快取過期前的持續時間。 預設TTL為6分鐘。

## 另請參閱 {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[目錄：:Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [屬性：:DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
