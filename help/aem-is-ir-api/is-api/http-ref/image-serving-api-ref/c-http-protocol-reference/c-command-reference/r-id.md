---
description: 映像/元資料版本。 當處理頻繁更改的內容時，快取網路（如Akamai、瀏覽器快取和公司代理伺服器快取）中的伺服器可以儲存可能在一段時間內過期的映像服務響應。
solution: Experience Manager
title: id
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3cdd27e4-14d2-42ef-aedb-9c1f7c39b4c6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 4%

---

# id{#id}

映像/元資料版本。 當處理頻繁更改的內容時，快取網路（如Akamai、瀏覽器快取和公司代理伺服器快取）中的伺服器可以儲存可能在一段時間內過期的映像服務響應。

` id= *`谷`*`

<table id="simpletable_3A6EBDA15B004636804E1ACEF952479A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 谷 </span> </span> </p> </td> 
  <td class="stentry"> <p>版本字串。 </p> </td> 
 </tr> 
</table>

影像服務包括版本化機制，其有助於減少應用程式使用過時的快取條目的機會。 此機制涉及使用 `req=props` 獲取影像資料和元資料（如影像映射或縮放目標資料）的版本標識符字串。 然後，版本標識符字串將添加到可快取的Image Service請求 `id=` 的子菜單。

當源映像或元資料更改時，相應的版本ID值也將更改。 包括具有 `id=` 命令可確保不再訪問舊快取條目。

下表列出了每個版本的版本標識符字串 `req=` 類型：

<table id="table_AE39BEBE18864880BBBF1C4F16785E2D"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> req=類型</b> </th> 
   <th class="entry"> <b> 來自req=props的版本標識符</b> </th> 
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
   <td> <p> 掩模 </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 目標 </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> TMB </p> </td> 
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

`req=` 上面未列出的類型具有短TTL( `attribute::NonImgExpiration`)或者他們的回答根本不可快取；沒有好處 `id=` 這些要求。

## 屬性 {#section-62e973d0d5884abebbb0679f9278ae2c}

請求屬性。 選擇性. 伺服器始終忽略。

## 預設 {#section-96136720c82842c89505347ec39e6024}

無。

## 範例 {#section-a5fb871e0ec8485c91c4fca78895d17f}

請參閱 [直接=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3) 例如用法。

## 請亦參閱 {#section-6b4befb47202415195a68516f60e9988}

[請求=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) 。 [直接=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)。 [目錄：：到期](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a)。 [屬性：:NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
