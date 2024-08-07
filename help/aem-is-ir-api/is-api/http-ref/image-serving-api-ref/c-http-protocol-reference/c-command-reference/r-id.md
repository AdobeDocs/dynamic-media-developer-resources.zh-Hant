---
title: id
description: 影像/中繼資料版本。 處理經常變更的內容時，快取網路（例如Akamai、瀏覽器快取和公司Proxy伺服器快取）中的伺服器可能會儲存影像伺服回應，這些回應可能會在一段時間內過期。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3cdd27e4-14d2-42ef-aedb-9c1f7c39b4c6
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 3%

---

# id{#id}

影像/中繼資料版本。 處理經常變更的內容時，快取網路（例如Akamai、瀏覽器快取和公司Proxy伺服器快取）中的伺服器可能會儲存影像伺服回應，這些回應可能會在一段時間內過期。

` id= *`值`*`

<table id="simpletable_3A6EBDA15B004636804E1ACEF952479A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">值</span> </span> </p> </td> 
  <td class="stentry"> <p>版本字串。 </p> </td> 
 </tr> 
</table>

「影像伺服」包含版本設定機制，有助於減少應用程式使用過時快取專案的機會。 此機制涉及使用`req=props`來取得影像資料和中繼資料（例如影像地圖或縮放目標資料）的版本識別碼字串。 然後使用`id=`命令將版本識別碼字串新增至可快取的「影像伺服」請求。

當來源影像或中繼資料變更時，對應的版本ID值也會變更。 使用`id=`命令包含最新的版本ID值，可確保無法再存取舊的快取專案。

下表列出用於每個`req=`型別的版本識別碼字串：

<table id="table_AE39BEBE18864880BBBF1C4F16785E2D"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> req= type</b> </th> 
   <th class="entry"> 來自req=props</b>的<b>版本識別碼 </th> 
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
   <td> <p> 遮色片 </p> </td> 
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
   <td> <p> 使用者資料 </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> xmp </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
 </tbody> 
</table>

以上未列出的`req=`型別可能有簡短的TTL ( `attribute::NonImgExpiration`)，或其回應完全無法快取；將`id=`加入這類要求沒有好處。

## 屬性 {#section-62e973d0d5884abebbb0679f9278ae2c}

要求屬性。 選填。 伺服器一律忽略。

## 預設 {#section-96136720c82842c89505347ec39e6024}

無。

## 範例 {#section-a5fb871e0ec8485c91c4fca78895d17f}

如需使用範例，請參閱[rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)的說明。

## 請亦參閱 {#section-6b4befb47202415195a68516f60e9988}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) ， [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)， [目錄：：Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a)， [屬性：：NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
