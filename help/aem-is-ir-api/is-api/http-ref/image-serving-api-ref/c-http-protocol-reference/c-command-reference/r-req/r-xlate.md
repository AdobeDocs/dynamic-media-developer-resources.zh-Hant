---
description: 可用的地區設定特定版本。 傳回請求路徑中指定之目錄ID的可用地區設定特定版本清單。
seo-description: 可用的地區設定特定版本。 傳回請求路徑中指定之目錄ID的可用地區設定特定版本清單。
seo-title: xlate
solution: Experience Manager
title: xlate
topic: Scene7 Image Serving - Image Rendering API
uuid: 4c2370e5-1d46-4242-89bb-a5ce416ef63c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# xlate{#xlate}

可用的地區設定特定版本。 傳回請求路徑中指定之目錄ID的可用地區設定特定版本清單。

`req=xlate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8970A3A5A64F4DC2B184E251993390C5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>唯一的請求識別碼。 </p></td> 
 </tr> 
</table>

請參 [閱物件Id轉譯](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414)。

例如：

`xlate.translatedIds=image,image_fr,image_de`

The HTTP response is cacheable with the TTL based on `catalog::Expiration`.

支援JSONP回應格式的請求可讓您使用參數的擴充語法來指定JS回呼處理常式 `req=` 的名稱：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JS回應中顯示的JS處理常式名稱。 僅允許a-z、A-Z和0-9字元。 選填。預設為 `s7jsonResponse`.
