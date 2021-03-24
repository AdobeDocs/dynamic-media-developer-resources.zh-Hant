---
description: 用戶端的快取存取時間。 到期前的小時數。 用於管理客戶端和代理伺服器快取。
solution: Experience Manager
title: 過期
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 1%

---


# 過期{#expiration}

用戶端的快取存取時間。 到期前的小時數。 用於管理客戶端和代理伺服器快取。

伺服器通過將此值添加到傳輸的時間／日期來計算NTTP響應資料的到期時間／日期。

瀏覽器使用檔案的過期時間來管理快取。 在將請求傳遞至伺服器之前，瀏覽器會檢查其快取，以查看檔案是否已下載。 如果是，且若檔案尚未過期，瀏覽器會傳送條件式GET要求（例如具有If-Modified-Since HTTP要求標題），而非一般GET要求。 伺服器可選擇以&#39;304&#39;狀態回應，而不傳送影像。 然後，瀏覽器只會從其快取載入檔案。 這可大幅提高經常存取資料的整體效能。

伺服器會將過期的HTTP回應標題設為目前的日期／時間加上最小的暈映：:Expiration and all catalog:::Expiration值（暈映和演算作業中涉及的所有材質）。

過期時間主要設定為影像資料回應。 某些類型的回應一律會標籤為立即到期（或標籤為不可快取），包括所有錯誤回應或屬性回覆。

## 屬性 {#section-e87e8f6b6d224c6ea2eeaad695c04be8}

實數、-2、-1、0或更大。 自回應影像產生後，到期前的小時數。 設為0，一律會立即使回應影像過期，這會有效停用用戶端快取。 設定為-1以標籤為`never expire`。 在這種情況下，伺服器會回應條件式`GET`要求而傳回304狀態（未修改），而不檢查檔案是否實際變更。 設定為-2以使用`attribute::Expiration`提供的預設設定。

## 預設 {#section-79d71706e12a4493a69d7febc3a1f271}

`attribute::Expiration` 如果欄位不存在、值為-2或欄位為空，則使用。

## 另請參閱 {#section-9d46a9d346fe42f3911edb3bd79f4121}

[屬性：:Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ,  [Vignette::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
