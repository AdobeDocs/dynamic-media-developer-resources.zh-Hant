---
description: 影像目錄中的影像集資料。 傳回URL路徑中指定之影像目錄項目的影像集資料。
solution: Experience Manager
title: 影像集
feature: Dynamic Media Classic, SDK/API，影像集
role: Developer,User
exl-id: 730e7db9-47f0-4e96-8948-18b8185a5b7a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---

# 影像集{#imageset}

影像目錄中的影像集資料。 傳回URL路徑中指定之影像目錄項目的影像集資料。

`req=imageset[,text|javascript|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 編碼</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>唯一請求識別碼。 </p></td> 
 </tr> 
</table>

返回`catalog::ImageSet`的內容時無需進一步修改（字串本地化除外，如果適用），後跟單行終止符(CR/LF)。 如果URL路徑未解析為有效的目錄項，則響應僅包含單行終結器。

請求字串中的其他命令會遭忽略。 HTTP回應可根據`catalog::NonImgExpiration`與TTL快取。

支援JSONP回應格式的要求可讓您使用`req=`參數的延伸語法來指定JS回呼處理常式的名稱：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP回應中出現的JS處理常式的名稱。僅允許a-z、A-Z和0-9個字元。 選填。預設為 `s7jsonResponse`.
