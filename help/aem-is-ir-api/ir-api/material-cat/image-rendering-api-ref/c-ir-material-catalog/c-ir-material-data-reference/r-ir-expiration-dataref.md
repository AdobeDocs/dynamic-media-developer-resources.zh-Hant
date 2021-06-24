---
description: 客戶端快取的存留時間。 到期前的小時數。 用於管理用戶端和代理伺服器快取。
solution: Experience Manager
title: 過期
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: e4f7e5a8-0021-4dd3-be1b-8cb656cabdac
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 1%

---

# 過期{#expiration}

客戶端快取的存留時間。 到期前的小時數。 用於管理用戶端和代理伺服器快取。

伺服器通過將此值添加到傳輸時間/日期來計算NTTP響應資料的到期時間/日期。

瀏覽器使用檔案的過期時間來管理快取。 在將要求傳遞至伺服器之前，瀏覽器會檢查其快取，查看檔案是否已下載。 若是，且檔案尚未過期，瀏覽器會傳送條件式GET要求（例如帶有If-Modified-Sine HTTP要求標題），而非一般GET要求。 伺服器可以選擇以「304」狀態響應，而不傳輸影像。 接著，瀏覽器只會從其快取中載入檔案。 這可大幅提升經常存取資料的整體效能。

伺服器會將過期的HTTP回應標頭設定為目前的日期/時間，加上最小的暈映：：過期和所有目錄：：過期值，以及轉譯操作中涉及的所有材料。

有效期主要針對影像資料回應而設定。 某些類型的回應一律會標示為立即過期（或標示為不可快取），包括所有錯誤回應或屬性回覆。

## 屬性 {#section-e87e8f6b6d224c6ea2eeaad695c04be8}

實數、-2、-1、0或更高。 自產生回應影像後直到過期的小時數。 設為0一律會立即讓回應影像過期，這會有效停用用戶端快取。 設為–1以標示為`never expire`。 在這種情況下，伺服器始終返回304狀態（未修改）以響應條件式`GET`請求，而不檢查檔案是否實際更改。 設為–2以使用`attribute::Expiration`提供的預設值。

## 預設 {#section-79d71706e12a4493a69d7febc3a1f271}

`attribute::Expiration` 如果欄位不存在、值為–2，或欄位為空，則會使用。

## 另請參閱 {#section-9d46a9d346fe42f3911edb3bd79f4121}

[屬性：：過期](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) , [暈映：：過期](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c), [請求=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
