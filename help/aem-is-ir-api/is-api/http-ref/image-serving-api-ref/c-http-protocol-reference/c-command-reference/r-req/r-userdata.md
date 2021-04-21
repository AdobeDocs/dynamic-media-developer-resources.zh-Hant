---
description: 影像目錄的使用者資料。 傳回URL路徑中指定之影像目錄項目的使用者資料。
solution: Experience Manager
title: 用戶資料
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 2%

---


# userdata{#userdata}

影像目錄的使用者資料。 傳回URL路徑中指定之影像目錄項目的使用者資料。

`req=userdata[,text|{xml[, *`編碼`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 編碼</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
</table>

返回`catalog::UserData`的內容。 當指定「text」格式時，`catalog::UserData`中`??`的所有實例都由行終結器替換，並在結尾附加一個行終結器(CR/LF)。 如果URL路徑未解析為有效的目錄條目，則響應僅由單行終結器組成。 請求「xml」或「json」格式時，會套用適當的格式。

請求字串中的其他命令會被忽略。

HTTP響應基於`catalog::Expiration`可以與TTL進行快取。

>[!NOTE]
>
>userdata屬性鍵名中不允許冒號字元。

支援JSONP回應格式的請求可讓您使用`req=`參數的擴充語法來指定JS回呼處理常式的名稱：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JS回應中顯示的JS處理常式名稱。僅允許a-z、A-Z和0-9字元。 選填。預設為 `s7jsonResponse`.
