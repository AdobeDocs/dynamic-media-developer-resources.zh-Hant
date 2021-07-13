---
description: 過期
solution: Experience Manager
title: 過期
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 064dab12-5f58-4e19-a6b1-fbd20182e3aa
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 2%

---

# 過期{#expiration}

用於管理用戶端和代理伺服器快取。 伺服器將此值加到傳輸的時間/日期，以計算HTTP回應資料的到期時間/日期。

瀏覽器使用檔案的過期時間來管理快取。 在將請求傳遞至伺服器之前，瀏覽器會檢查其快取，查看檔案是否已下載。 若是，且檔案尚未過期，瀏覽器會傳送條件式GET要求（例如在要求標題中設定If-Modified-Since欄位），而非一般GET要求。 伺服器可以選擇以「304」狀態響應，而不傳輸影像。 接著，瀏覽器會從其快取中載入檔案。 這可大幅提升經常存取資料的整體效能。

這些回應類型會使用過期時間：

* `req=img`
* `req=mask`
* `req=tmb`
* `req=userdata`
* `req=map`

某些類型的回應（例如錯誤回應）一律會標示為立即過期（或標示為不可快取），而其他類型（例如屬性或預設影像回應）則使用特殊的過期設定（`attribute::NonImgExpiration`和`attribute::DefaultExpiration`）。

## 屬性 {#section-7f5173d090cf48df8fa1a2c72b8c8c60}

實數、-2、-1或0或更高。 自產生回應影像後直到過期的小時數。 設為0一律會立即讓回覆影像過期，這會有效停用用戶端快取。 設為–1以標示為&#x200B;*`never expire`*。 在這種情況下，伺服器一律會傳回304狀態（未修改）以回應條件式GET請求，而不檢查檔案是否實際變更。 設為–2以使用`attribute::Expiration`提供的預設值。

## 預設 {#section-ec72cc1dfc5e4f278174d37da2e39462}

`attribute::Expiration` 如果欄位不存在、值為–2，或欄位為空，則會使用。

## 另請參閱 {#section-0e5e8595aad641c689726828712a8902}

[attribute::Expiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7),  [attribute::DefaultExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf),  [attribute::NonImgExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d),  [req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
