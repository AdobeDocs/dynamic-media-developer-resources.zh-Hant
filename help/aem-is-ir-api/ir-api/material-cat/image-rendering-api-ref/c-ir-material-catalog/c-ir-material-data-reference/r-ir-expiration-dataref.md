---
title: 過期
description: 客戶端快取生存時間。 到期前的小時數。 用於管理客戶端和代理伺服器快取。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4f7e5a8-0021-4dd3-be1b-8cb656cabdac
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 過期{#expiration}

客戶端快取生存時間。 到期前的小時數。 用於管理客戶端和代理伺服器快取。

伺服器通過將此值添加到傳輸的時間/日期來計算NTTP響應資料的到期時間/日期。

瀏覽器使用檔案的過期時間管理快取。 在將請求傳遞到伺服器之前，瀏覽器將檢查其快取，以查看檔案是否已下載。 如果是，並且檔案尚未過期，則瀏覽器將發送條件GET請求（例如帶有If-Modified-Sine HTTP請求標頭），而不是普通GET請求。 伺服器可以選擇以「304」狀態響應而不傳輸映像。 然後，瀏覽器將只從其快取中載入檔案。 這可以顯著提高頻繁訪問資料的整體效能。

伺服器會將過期HTTP響應標頭設定為當前日期/時間加上最小的卷：:Expiration和所有目錄：:Expiration值，用於卷和呈現操作中涉及的所有材料。

過期主要為影像資料響應設定。 某些類型的響應將始終標籤為立即過期（或標籤為不可快取），包括所有錯誤響應或屬性答復。

## 屬性 {#section-e87e8f6b6d224c6ea2eeaad695c04be8}

實數、-2、-1、0或更大。 自生成響應映像以來到期的小時數。 設定為0以始終立即使響應映像過期，這將有效地禁用客戶端快取。 設定為–1以標籤為 `never expire`。 在這種情況下，伺服器始終返回304狀態（未修改）以響應條件 `GET` 請求，但不檢查檔案是否已實際更改。 設定為–2以使用由 `attribute::Expiration`。

## 預設 {#section-79d71706e12a4493a69d7febc3a1f271}

`attribute::Expiration` 如果欄位不存在，如果值為–2，或者欄位為空，則使用。

## 另請參閱 {#section-9d46a9d346fe42f3911edb3bd79f4121}

[屬性：：到期](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) 。 [vignette:：到期](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)。 [請求=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
