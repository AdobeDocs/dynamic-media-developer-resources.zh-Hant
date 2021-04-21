---
description: 縮放以影像目錄中的資料為目標。 傳回URL路徑中指定之影像目錄項目的縮放目標資料。
solution: Experience Manager
title: 目標
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 2%

---


# 目標{#targets}

縮放以影像目錄中的資料為目標。 傳回URL路徑中指定之影像目錄項目的縮放目標資料。

`req=targets[,text|{xml[, *`EncodingreqId`*]}|{json[&id= *``*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 編碼</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>唯一的請求識別碼。 </p></td> 
 </tr> 
</table>

返回`catalog::Targets`的內容。 當請求「text」格式時，`catalog::Targets`中的所有`??`實例都由行終結器替換，並在結尾附加一個行終結器(`CR/LF`)。 如果URL路徑未解析為有效的目錄條目，則響應僅由單行終結器組成。 請求「xml」或「json」格式時，會套用適當的格式。

請求字串中的其他命令會被忽略。

HTTP響應基於`catalog::Expiration`可以與TTL進行快取。

支援JSONP回應格式的請求可讓您使用`req=`參數的擴充語法來指定JS回呼處理常式的名稱：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JS回應中顯示的JS處理常式名稱。僅允許a-z、A-Z和0-9字元。 選填。預設為 `s7jsonResponse`.
