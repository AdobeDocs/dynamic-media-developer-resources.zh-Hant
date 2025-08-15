---
description: 縮放影像目錄中的目標資料。 針對URL路徑中指定的影像目錄專案，傳回縮放目標資料。
solution: Experience Manager
title: 目標
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58f7b1ad-8762-4d23-b320-6f69e75ecf63
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---

# 目標{#targets}

縮放影像目錄中的目標資料。 針對URL路徑中指定的影像目錄專案，傳回縮放目標資料。

`req=targets[,text|{xml[, *`編碼`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname">編碼</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>唯一要求識別碼。 </p></td> 
 </tr> 
</table>

已傳回`catalog::Targets`的內容。 要求&#39;text&#39;格式時，`??`中`catalog::Targets`的所有執行個體都會取代為行終止元，而單行終止元(`CR/LF`)會附加至結尾。 如果URL路徑無法解析為有效的目錄專案，回應只會包含單行終止元。 要求&#39;xml&#39;或&#39;json&#39;格式時，會套用適當的格式。

會忽略請求字串中的其他命令。

HTTP回應可使用以`catalog::Expiration`為基礎的TTL進行快取。

支援JSONP回應格式的請求可讓您使用`req=`引數的延伸語法來指定JS回呼處理常式的名稱：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`是JSONP回應中出現的JS處理常式名稱。 僅允許a-z、A-Z和0-9字元。 選填。 預設值為`s7jsonResponse`。
