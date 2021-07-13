---
description: 縮放目標影像目錄中的資料。 傳回URL路徑中指定之影像目錄項目的縮放目標資料。
solution: Experience Manager
title: 目標
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58f7b1ad-8762-4d23-b320-6f69e75ecf63
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 2%

---

# 目標{#targets}

縮放目標影像目錄中的資料。 傳回URL路徑中指定之影像目錄項目的縮放目標資料。

`req=targets[,text|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 編碼</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>唯一請求識別碼。 </p></td> 
 </tr> 
</table>

返回`catalog::Targets`的內容。 請求「text」格式時，`catalog::Targets`中`??`的所有實例都被行終結器替換，並且結尾附加一個行終結器(`CR/LF`)。 如果URL路徑未解析為有效的目錄項，則響應僅包含單行終結器。 請求「xml」或「json」格式時，會套用適當的格式。

請求字串中的其他命令會遭忽略。

HTTP回應可根據`catalog::Expiration`與TTL快取。

支援JSONP回應格式的要求可讓您使用`req=`參數的延伸語法來指定JS回呼處理常式的名稱：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP回應中出現的JS處理常式的名稱。僅允許a-z、A-Z和0-9個字元。 選填。預設為 `s7jsonResponse`.
