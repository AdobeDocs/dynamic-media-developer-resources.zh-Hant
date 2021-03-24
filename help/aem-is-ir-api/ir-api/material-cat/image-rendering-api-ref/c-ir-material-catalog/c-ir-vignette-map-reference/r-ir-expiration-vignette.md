---
description: 用戶端的快取存取時間。 到期前的小時數。 用於管理客戶端和代理伺服器快取。
solution: Experience Manager
title: 過期
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 6%

---


# 過期{#expiration}

用戶端的快取存取時間。 到期前的小時數。 用於管理客戶端和代理伺服器快取。

如需詳細資訊，請參閱` [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)`。

## 屬性 {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

實數、-2、-1、0或更大。 自回應影像產生後，到期前的小時數。 設為0，一律會立即使回應影像過期，這會有效停用用戶端快取。 設定為-1以標籤為`never expire`;在這種情況下，伺服器會隨時回覆403狀態，以回應條件式`GET`要求，而不檢查檔案是否實際變更。 設定為-2以使用`attribute::Expiration`提供的預設設定。

## 預設 {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration` 如果欄位不存在、值為-2或欄位為空，則使用。

## 另請參閱 {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[屬性：:Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ,  [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
