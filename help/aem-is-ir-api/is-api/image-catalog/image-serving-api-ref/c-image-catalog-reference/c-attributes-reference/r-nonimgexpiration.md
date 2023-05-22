---
description: 非映像響應的客戶端快取TTL。 為某些非映像響應提供過期間隔。
solution: Experience Manager
title: 非Img到期
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c61e2781-dfaa-4f3d-958d-5ffa755a3e4d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 2%

---

# 非Img到期{#nonimgexpiration}

非映像響應的客戶端快取TTL。 為某些非映像響應提供過期間隔。

為某些非映像響應（包括響應以下命令發送的響應）提供過期間隔：

* `req=imageset`
* `req=catalogprops`
* `req=exists`
* `req=imageprops`
* `req=props`

## 屬性 {#section-d37e3113f4b1468b86b5a14e80d94c83}

實數，0或更大。 自生成回復資料以來到期的小時數。 設定為0時，始終立即使回復映像過期，這將有效地禁用預設映像響應的客戶端快取。 設定為–1以標籤為 *永遠*。

## 預設 {#section-96981360c0234b7f824d2ff7c25a7954}

繼承自 `default::NonImgExpiration` 或為空。

TTL(Time-To-Live)是快取過期前的持續時間。 預設TTL為6分鐘。

## 另請參閱 {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[目錄：：到期](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) 。 [屬性：:DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
