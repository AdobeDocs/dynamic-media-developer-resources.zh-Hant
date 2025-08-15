---
description: 過期
solution: Experience Manager
title: 過期
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 62d2368b-ea56-4964-ab9c-07454e19540c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 2%

---

# 過期{#expiration}

用來管理使用者端和Proxy伺服器快取。 伺服器會將此值與傳輸時間/日期相加，以計算HTTP回應資料的到期時間/日期。

瀏覽器會使用檔案的到期時間來管理快取。 將請求傳遞至伺服器之前，瀏覽器會檢查其快取，檢視檔案是否已下載。 若是如此，且檔案尚未過期，瀏覽器會傳送條件式GET要求（例如在要求標題中設定If-Modified-Since欄位），而非一般GET要求。 伺服器可以選擇以&#39;304&#39;狀態回應，而不傳輸影像。 然後瀏覽器會從其快取載入檔案。 這可能會大幅提升經常存取資料的整體效能。

到期適用於這些回應型別：

* `req=img`
* `req=mask`
* `req=tmb`
* `req=userdata`
* `req=map`

某些型別的回應（例如，錯誤回應）一律會標示為立即到期（或標籤為不可快取），而其他型別（例如，屬性或預設影像回應）則使用特殊的到期設定（`attribute::NonImgExpiration`和`attribute::DefaultExpiration`）。

## 屬性 {#section-7f5173d090cf48df8fa1a2c72b8c8c60}

實數、-2、-1或0或更大。 從產生回應影像到到期為止的小時數。 設為0可一律使回覆影像立即過期，以有效停用使用者端快取。 設為–1以標籤為&#x200B;*`never expire`*。 在此情況下，伺服器一律會回應條件式GET要求傳回304狀態（未修改），而不會檢查檔案是否實際變更。 設定為–2以使用`attribute::Expiration`提供的預設值。

## 預設 {#section-ec72cc1dfc5e4f278174d37da2e39462}

如果欄位不存在、值為–2或欄位為空，則會使用`attribute::Expiration`。

## 另請參閱 {#section-0e5e8595aad641c689726828712a8902}

[attribute：：Expiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7)，[attribute：：DefaultExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)，[attribute：：NonImgExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)，[req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
