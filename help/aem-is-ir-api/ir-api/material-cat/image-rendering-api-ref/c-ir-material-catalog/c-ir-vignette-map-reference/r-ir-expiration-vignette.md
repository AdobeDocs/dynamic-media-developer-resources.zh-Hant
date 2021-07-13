---
description: 客戶端快取的存留時間。 到期前的小時數。 用於管理用戶端和代理伺服器快取。
solution: Experience Manager
title: 過期
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5717d568-467e-495b-b963-9b3d42e866a6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 6%

---

# 過期{#expiration}

客戶端快取的存留時間。 到期前的小時數。 用於管理用戶端和代理伺服器快取。

如需詳細資訊，請參閱` [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)`。

## 屬性 {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

實數、-2、-1、0或更高。 自產生回應影像後直到過期的小時數。 設為0一律會立即讓回應影像過期，這會有效停用用戶端快取。 設為–1以標籤為`never expire`;在這種情況下，伺服器會一律回應條件式`GET`要求而傳回403狀態，而不檢查檔案是否實際已變更。 設為–2以使用`attribute::Expiration`提供的預設值。

## 預設 {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration` 如果欄位不存在、值為–2，或欄位為空，則會使用。

## 另請參閱 {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[屬性：：過期](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ，目 [錄：：過期](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
