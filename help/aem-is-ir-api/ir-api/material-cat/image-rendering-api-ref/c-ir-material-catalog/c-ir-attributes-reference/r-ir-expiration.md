---
description: 預設的客戶端快取存留時間。 提供預設過期時間間隔，以備特定目錄記錄不包含有效的目錄過期值或暈映過期值，或直接訪問暈映檔案或物料檔案時使用，而不是通過目錄記錄。
solution: Experience Manager
title: 過期
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 6d9cca06-f675-4ae4-a187-9cd716e7c554
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 3%

---

# 過期{#expiration}

預設的客戶端快取存留時間。 提供預設過期時間間隔，以備特定目錄記錄不包含有效目錄：：過期或暈映：：過期值，或直接訪問暈映檔案或物料檔案（而非通過目錄記錄）時使用。

## 屬性 {#section-8e2bade105ec4905ae5c4911f500279f}

實數，0或更高。 自回覆資料產生以來直到到期的小時數。 設為0一律會立即讓回覆影像過期，這會有效停用用戶端快取。 設為–1以標示為&#x200B;*永不過期*。

## 預設 {#section-18cfce46edb441bfae7dd9d3e0217ba9}

繼承自預設：：如果未定義或為空，則過期。

## 另請參閱 {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[目錄：：過期](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) ，暈 [映：：過期](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
