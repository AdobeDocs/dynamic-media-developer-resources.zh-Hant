---
description: 過期
solution: Experience Manager
title: 過期
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 2%

---


# 過期{#expiration}

用於管理客戶端和代理伺服器快取。 伺服器通過將此值添加到傳輸的時間／日期來計算HTTP響應資料的到期時間／日期。

瀏覽器使用檔案的過期時間來管理快取。 在將請求傳遞至伺服器之前，瀏覽器會檢查其快取，以查看檔案是否已下載。 如果是，且檔案尚未過期，瀏覽器會傳送條件式GET要求（例如在請求標題中設定If-Modified-Since欄位），而非一般GET要求。 伺服器可選擇以&#39;304&#39;狀態回應，而不傳送影像。 然後瀏覽器會從其快取載入檔案。 這可大幅提高經常存取資料的整體效能。

過期時間用於以下響應類型：

* `req=img`
* `req=mask`
* `req=tmb`
* `req=userdata`
* `req=map`

某些類型的回應（例如錯誤回應）一律會標籤為立即到期（或標籤為不可快取），而其他回應（例如屬性或預設影像回應）則會使用特殊的過期設定（`attribute::NonImgExpiration`和`attribute::DefaultExpiration`）。

## 屬性 {#section-7f5173d090cf48df8fa1a2c72b8c8c60}

實數、-2、-1或0或更高。 自回應影像產生後，到期前的小時數。 設為0，一律會立即使回覆影像過期，這會有效停用用戶端快取。 設定為-1以標籤為&#x200B;*`never expire`*。 在這種情況下，伺服器會回應條件式GET要求，而一律傳回304狀態（未修改），而不檢查檔案是否實際變更。 設定為-2以使用`attribute::Expiration`提供的預設設定。

## 預設 {#section-ec72cc1dfc5e4f278174d37da2e39462}

`attribute::Expiration` 如果欄位不存在、值為-2或欄位為空，則使用。

## 另請參閱 {#section-0e5e8595aad641c689726828712a8902}

[attribute::Expiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7),  [attribute::DefaultExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf),  [attribute::NonImgExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d),  [req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
