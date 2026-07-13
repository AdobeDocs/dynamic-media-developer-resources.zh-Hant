---
title: 過期
description: 預設使用者端快取存留時間。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6d9cca06-f675-4ae4-a187-9cd716e7c554
TQID: 'https://experienceleague.adobe.com/UkPYVP3aAoseZcXo5zLTVIiejTIPv5HXHekcIgS-B4U'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 103
ht-degree: 4%

---

# 過期{#expiration}

預設使用者端快取存留時間。 提供預設到期間隔，以防止特定目錄記錄未包含有效的`catalog::Expiration`或`vignette::Expiration`值。 或者，如果直接存取暈映檔案或材料檔案，而不是透過目錄記錄存取。

## 屬性 {#section-8e2bade105ec4905ae5c4911f500279f}

實數，`0`或更大。 從產生回覆資料到到期為止的小時數。 設定為`0`可一律讓回覆影像立即過期，以有效停用使用者端快取。 設定為`-1`以標籤為&#x200B;*永不過期*。

## 預設 {#section-18cfce46edb441bfae7dd9d3e0217ba9}

如果未定義或空白，則繼承自`default::Expiration`。

## 另請參閱 {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[目錄：：Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) ， [暈映：：Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)

