---
description: 過期
solution: Experience Manager
title: 過期
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 064dab12-5f58-4e19-a6b1-fbd20182e3aa
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 2%

---

# 過期{#expiration}

用於管理客戶端和代理伺服器快取。 伺服器通過將此值添加到傳輸的時間/日期來計算HTTP響應資料的到期時間/日期。

瀏覽器使用檔案的過期時間管理快取。 在將請求傳遞到伺服器之前，瀏覽器會檢查其快取，以查看檔案是否已下載。 如果是，並且檔案尚未過期，則瀏覽器會發送條件GET請求（例如，在請求標題中設定了If-Modified-Sine欄位），而不是普通GET請求。 伺服器可以選擇以「304」狀態響應而不傳輸映像。 然後，瀏覽器從其快取中載入檔案。 這可以顯著提高頻繁訪問資料的整體效能。

到期日用於以下響應類型：

* `req=img`
* `req=mask`
* `req=tmb`
* `req=userdata`
* `req=map`

某些類型的響應（如錯誤響應）始終被標籤為立即過期（或標籤為不可快取），而其他響應（如屬性或預設映像響應）則使用特殊的過期設定( `attribute::NonImgExpiration` 和 `attribute::DefaultExpiration`)。

## 屬性 {#section-7f5173d090cf48df8fa1a2c72b8c8c60}

實數、-2、-1或0或更大。 自生成響應映像以來到期的小時數。 設定為0時，始終立即使回復映像過期，這將有效地禁用客戶端快取。 設定為–1以標籤為 *`never expire`*。 在這種情況下，伺服器始終返回304狀態（未修改）以響應條件GET請求，而不檢查檔案是否確實已更改。 設定為–2以使用由 `attribute::Expiration`。

## 預設 {#section-ec72cc1dfc5e4f278174d37da2e39462}

`attribute::Expiration` 如果欄位不存在，如果值為–2，或者欄位為空，則使用。

## 另請參閱 {#section-0e5e8595aad641c689726828712a8902}

[屬性：：到期](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7)。 [屬性：:DefaultExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)。 [屬性：:NonImgExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)。 [請求=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
