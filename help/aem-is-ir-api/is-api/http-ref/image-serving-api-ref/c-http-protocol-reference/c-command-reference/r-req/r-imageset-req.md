---
description: 影像目錄的影像集資料。 傳回URL路徑中指定之影像目錄項目的影像集資料。
solution: Experience Manager
title: 影像集
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 2%

---


# imageset{#imageset}

影像目錄的影像集資料。 傳回URL路徑中指定之影像目錄項目的影像集資料。

`req=imageset[,text|javascript|{xml[, *`EncodingreqId`*]}|{json[&id= *``*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 編碼</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>唯一的請求識別碼。 </p></td> 
 </tr> 
</table>

傳回`catalog::ImageSet`的內容時，不需進一步修改（字串本地化除外，如果適用），後面接著單行終結器(CR/LF)。 如果URL路徑未解析為有效的目錄條目，則響應僅由單行終結器組成。

請求字串中的其他命令會被忽略。 HTTP響應基於`catalog::NonImgExpiration`可以與TTL進行快取。

支援JSONP回應格式的請求可讓您使用`req=`參數的擴充語法來指定JS回呼處理常式的名稱：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JS回應中顯示的JS處理常式名稱。僅允許a-z、A-Z和0-9字元。 選填。預設為 `s7jsonResponse`.
