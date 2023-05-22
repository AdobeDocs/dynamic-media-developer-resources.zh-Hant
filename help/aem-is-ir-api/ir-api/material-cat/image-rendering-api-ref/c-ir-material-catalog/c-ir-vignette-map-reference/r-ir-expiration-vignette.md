---
description: 客戶端快取生存時間。 到期前的小時數。 用於管理客戶端和代理伺服器快取。
solution: Experience Manager
title: 過期
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5717d568-467e-495b-b963-9b3d42e866a6
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---

# 過期{#expiration}

客戶端快取生存時間。 到期前的小時數。 用於管理客戶端和代理伺服器快取。

請參閱 [目錄：：到期](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md) 的雙曲餘切值。

## 屬性 {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

實數、-2、-1、0或更大。 自生成響應映像以來到期的小時數。 設定為0以始終立即使響應映像過期，這將有效地禁用客戶端快取。 設定為–1以標籤為 `never expire`;在這種情況下，伺服器始終返回403狀態以響應條件 `GET` 請求，但不檢查檔案是否已實際更改。 設定為–2以使用由 `attribute::Expiration`。

## 預設 {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration` 如果欄位不存在，如果值為–2，或者欄位為空，則使用。

## 另請參閱 {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[屬性：：到期](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) 。 [目錄：：到期](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)。 [請求=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
