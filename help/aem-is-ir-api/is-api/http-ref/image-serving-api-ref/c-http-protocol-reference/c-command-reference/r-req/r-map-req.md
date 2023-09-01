---
title: 地圖
description: 影像地圖資料。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 4%

---

# 地圖{#map}

影像地圖資料。

`req=map[,text|{xml[, *`編碼`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 編碼</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>唯一要求識別碼。 </p></td> 
 </tr> 
</table>

傳回 `catalog::Map` 查詢簡單目錄專案時未進行修改，未指定其他命令(不會縮放為 `catalog::maxPix`)。

如果在要求中指定了任何其他命令，則會傳回複合影像對應。 複合影像地圖是透過縮放、裁切、旋轉及全部圖層化所衍生 `catalog::Map` 和/或 `map=` 要求中包含的命令，就像影像資料會使用一樣 `req=img`.

指定 `text` 或省略第二個引數，讓您可以傳回形式為的影像地圖資料 `HTML <AREA>` 具有回應MIME型別的元素字串 `text/plain`.

指定 `xml` 因此您可以將回應格式化為XML，而非HTML。 可選擇指定文字編碼。 預設值為 `UTF-8`.

傳回空字串（或空白） `<AREA>` 元素)，如果沒有找到指定目錄物件的對應資料，和/或沒有 `<AREA>` 裁切影像後，元素仍會保留。

HTTP回應可使用以下依據的TTL進行快取： `catalog::Expiration`.

支援JSONP回應格式的請求可讓您使用擴充語法來指定JS回呼處理常式的名稱 `req=` 引數：

`req=...,json [&handler = reqHandler ]`

此 `<reqHandler>` 是JSONP回應中出現的JS處理常式名稱。 僅允許a-z、A-Z和0-9字元。 選擇性. 預設值為 `s7jsonResponse`.

另請參閱 [影像地圖](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
