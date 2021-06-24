---
description: 來自映像目錄的用戶資料。 傳回url路徑中指定之影像目錄項目的使用者資料。
solution: Experience Manager
title: userdata
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: b1d85ea6-0e12-49a8-b1dc-4c64a672770b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 2%

---

# userdata{#userdata}

來自映像目錄的用戶資料。 傳回url路徑中指定之影像目錄項目的使用者資料。

`req=userdata[,text|{xml[, *`編碼`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 編碼</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
</table>

返回`catalog::UserData`的內容。 當指定「text」格式時，`catalog::UserData`中`??`的所有實例都被行終結器替換，並且結尾附加一個單行終結器(CR/LF)。 如果URL路徑未解析為有效的目錄項，則響應僅包含單行終結器。 請求「xml」或「json」格式時，會套用適當的格式。

請求字串中的其他命令會遭忽略。

HTTP回應可根據`catalog::Expiration`與TTL快取。

>[!NOTE]
>
>userdata屬性索引鍵名稱中不允許使用冒號字元。

支援JSONP回應格式的要求可讓您使用`req=`參數的延伸語法來指定JS回呼處理常式的名稱：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP回應中出現的JS處理常式的名稱。僅允許a-z、A-Z和0-9個字元。 選填。預設為 `s7jsonResponse`.
