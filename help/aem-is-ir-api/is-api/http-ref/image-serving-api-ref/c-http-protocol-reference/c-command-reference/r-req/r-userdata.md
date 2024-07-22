---
description: 影像目錄中的使用者資料。 傳回URL路徑中所指定影像目錄專案的使用者資料。
solution: Experience Manager
title: 使用者資料
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b1d85ea6-0e12-49a8-b1dc-4c64a672770b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# 使用者資料{#userdata}

影像目錄中的使用者資料。 傳回URL路徑中所指定影像目錄專案的使用者資料。

`req=userdata[,text|{xml[, *`編碼`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">編碼</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
</table>

已傳回`catalog::UserData`的內容。 指定&#39;text&#39;格式時，`catalog::UserData`中`??`的所有執行個體都會被行終止元取代，而單行終止元(CR/LF)會附加在結尾處。 如果URL路徑無法解析為有效的目錄專案，回應只會包含單行終止元。 要求&#39;xml&#39;或&#39;json&#39;格式時，會套用適當的格式。

會忽略請求字串中的其他命令。

HTTP回應可使用以`catalog::Expiration`為基礎的TTL進行快取。

>[!NOTE]
>
>userdata屬性索引鍵名稱中不允許冒號字元。

支援JSONP回應格式的請求可讓您使用`req=`引數的延伸語法來指定JS回呼處理常式的名稱：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`是JSONP回應中出現的JS處理常式名稱。 僅允許a-z、A-Z和0-9字元。 選填。 預設值為`s7jsonResponse`。
