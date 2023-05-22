---
description: 來自映像目錄的用戶資料。 返回URL路徑中指定的影像目錄條目的用戶資料。
solution: Experience Manager
title: 用戶資料
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b1d85ea6-0e12-49a8-b1dc-4c64a672770b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 2%

---

# 用戶資料{#userdata}

來自映像目錄的用戶資料。 返回URL路徑中指定的影像目錄條目的用戶資料。

`req=userdata[,text|{xml[, *`編碼`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 編碼</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
</table>

內容 `catalog::UserData` 的子菜單。 當指定「text」格式時， `??` 在 `catalog::UserData`替換為行終止器，並在末端附加單行終止器(CR/LF)。 如果URL路徑未解析為有效的目錄條目，則響應僅由單行終結器組成。 請求「xml」或「json」格式時應用適當的格式。

請求字串中的其他命令將被忽略。

HTTP響應可以與基於的TTL進行快取 `catalog::Expiration`。

>[!NOTE]
>
>userdata屬性鍵名中不允許冒號字元。

支援JSONP響應格式的請求允許您使用擴展語法指定JS回調處理程式的名稱 `req=` 參數：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP響應中存在的JS處理程式的名稱。 只允許使用a-z、A-Z和0-9個字元。 選擇性. 預設為 `s7jsonResponse`.
