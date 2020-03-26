---
description: 媒體設定資訊。
seo-description: 媒體設定資訊。
seo-title: 設定
solution: Experience Manager
title: 設定
topic: Scene7 Image Serving - Image Rendering API
uuid: ebd78249-45ea-47cd-8845-786070f92f21
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 設定{#set}

媒體設定資訊。

req=set[,xml[, *`encoding`*]|{json[&amp;id=*`reqId`*]}]

<table id="simpletable_02C955F4EBAD4251A728F0FC68F432B5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 編碼</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> reqId</span> </p></td> 
  <td class="stentry"> <p>唯一的請求識別碼 </p></td> 
 </tr> 
</table>

傳回與目錄：:ImageSet相關的影像、視訊、色票和各種中繼資料，以取得URL路徑中指定之影像目錄項目的相關資訊。 該響應是由提供的集合類型確定的分層結構。 請求「xml」或「json」格式時，會套用適當的格式。

The HTTP response is cacheable with the TTL based on `catalog::NonImgExpiration`.

>[!NOTE]
>
>req=set請求中不允許冒號字元。

支援JSON回應格式的請求可讓您使用參數的擴充語法來指定JS回呼處理常式的 `req=` 名稱：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP回應中顯示的JS處理常式名稱。 僅允許a-z、A-Z和0-9字元。 選填。預設為 `s7jsonResponse`.
