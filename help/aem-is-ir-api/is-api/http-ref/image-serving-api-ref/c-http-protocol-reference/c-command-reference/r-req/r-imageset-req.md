---
description: 影像目錄中的影像集資料。 針對URL路徑中指定的影像目錄專案，傳回影像集資料。
solution: Experience Manager
title: 影像集
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: 730e7db9-47f0-4e96-8948-18b8185a5b7a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 2%

---

# 影像集{#imageset}

影像目錄中的影像集資料。 針對URL路徑中指定的影像目錄專案，傳回影像集資料。

`req=imageset[,text|javascript|{xml[, *`編碼`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 編碼</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>唯一要求識別碼。 </p></td> 
 </tr> 
</table>

的內容 `catalog::ImageSet` 會傳回而不作進一步的修改（字串本地化除外，如果適用的話），後面接著單行終止元(CR/LF)。 如果URL路徑無法解析為有效的目錄專案，回應只會包含單行終止元。

會忽略請求字串中的其他命令。 HTTP回應可使用以下依據的TTL進行快取： `catalog::NonImgExpiration`.

支援JSONP回應格式的請求可讓您使用擴充語法來指定JS回呼處理常式的名稱 `req=` 引數：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP回應中出現的JS處理常式名稱。 僅允許a-z、A-Z和0-9字元。 選擇性. 預設為 `s7jsonResponse`.
