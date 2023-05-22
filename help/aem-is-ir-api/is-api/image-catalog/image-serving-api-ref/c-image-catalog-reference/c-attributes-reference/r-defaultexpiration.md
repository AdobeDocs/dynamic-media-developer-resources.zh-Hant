---
description: 預設映像響應的客戶端快取TTL。 提供預設映像響應（返回用defaultImage=或屬性DefaultImage指定的預設映像的響應）的過期間隔。
solution: Experience Manager
title: 預設到期
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 99103681-c00c-4648-8dee-2314e7e614af
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 1%

---

# 預設到期{#defaultexpiration}

預設映像響應的客戶端快取TTL。 提供預設映像響應（返回用defaultImage=或attribute::DefaultImage指定的預設映像的響應）的過期間隔。

僅當預設影像未與目錄記錄關聯或預設影像目錄記錄未提供特定時應用 `catalog::Expiration` 值。

## 屬性 {#section-e564512476604fd7b964f9f2903d6d33}

實數，0或更大。 自生成回復資料以來到期的小時數。 設定為0時，始終立即使回復映像過期，這將有效地禁用預設映像響應的客戶端快取。 設定為 `-1` 標籤為 `never expire`。

## 預設 {#section-131cd32c2e214391857dba5af321f8cd}

繼承自 `default::DefaultExpiration` 或為空。

TTL(Time-To-Live)是快取過期前的持續時間。 預設TTL為1小時。

## 另請參閱 {#section-d8642c22e3d947129367dd76366963d6}

[目錄：：到期](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) 。 [屬性：:DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
