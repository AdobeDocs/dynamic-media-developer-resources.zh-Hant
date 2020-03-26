---
description: 影像／中繼資料版本。 當處理經常變更的內容時，快取網路（例如Akamai、瀏覽器快取和公司代理伺服器快取）中的伺服器可儲存影像伺服回應，其可能已過時一段時間。
seo-description: 影像／中繼資料版本。 當處理經常變更的內容時，快取網路（例如Akamai、瀏覽器快取和公司代理伺服器快取）中的伺服器可儲存影像伺服回應，其可能已過時一段時間。
seo-title: id
solution: Experience Manager
title: id
topic: Scene7 Image Serving - Image Rendering API
uuid: 3d526326-c8fa-4aef-95a9-93ccacf08f73
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# id{#id}

影像／中繼資料版本。 當處理經常變更的內容時，快取網路（例如Akamai、瀏覽器快取和公司代理伺服器快取）中的伺服器可儲存影像伺服回應，其可能已過時一段時間。

` id= *`val`*`

<table id="simpletable_3A6EBDA15B004636804E1ACEF952479A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> val </span></span> </p> </td> 
  <td class="stentry"> <p>版本字串。 </p> </td> 
 </tr> 
</table>

「影像伺服」包含版本修訂機制，可協助降低應用程式使用過時快取項目的機率。 此機制涉及使 `req=props` 用取得影像資料和中繼資料的版本識別碼字串（例如影像地圖或縮放目標資料）。 版本識別碼字串隨後會以命令新增至可快取的影像伺服 `id=` 請求。

當來源影像或中繼資料變更時，對應的版本ID值也會變更。 在命令中包含最新的版本ID值可確 `id=` 保不再訪問舊的快取條目。

下表列出了用於每種類型的版本標識符 `req=` 字串：

<table id="table_AE39BEBE18864880BBBF1C4F16785E2D"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> req=類型</b> </th> 
   <th class="entry"> <b> req=props的版本識別碼</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> img </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 地圖 </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 遮罩 </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 目標 </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> tmb </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 用戶資料 </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> xmp </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
 </tbody> 
</table>

`req=` 上面未列出的類型有較短的TTL( `attribute::NonImgExpiration`)，或者它們的響應根本不可快取；納入此類要求並 `id=` 無好處。

## 屬性 {#section-62e973d0d5884abebbb0679f9278ae2c}

請求屬性。 選填。伺服器始終忽略。

## 預設 {#section-96136720c82842c89505347ec39e6024}

無。

## 範例 {#section-a5fb871e0ec8485c91c4fca78895d17f}

請參閱rect= [的說明](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3) ，例如用法。

## 請亦參閱 {#section-6b4befb47202415195a68516f60e9988}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) , [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3), [catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a), [attribute::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
