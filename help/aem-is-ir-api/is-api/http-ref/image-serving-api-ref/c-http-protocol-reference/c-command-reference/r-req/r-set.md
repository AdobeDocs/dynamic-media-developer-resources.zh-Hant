---
description: 媒體集資訊。
solution: Experience Manager
title: 設定
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bc69f094-ff21-4dd7-9e10-daddb3de0c65
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 4%

---

# 設定{#set}

媒體集資訊。

req=set[,xml[。 *`encoding`*]|json[&amp;id=*`reqId`*]}]

<table id="simpletable_02C955F4EBAD4251A728F0FC68F432B5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 編碼</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> reqId</span> </p></td> 
  <td class="stentry"> <p>唯一請求標識符 </p></td> 
 </tr> 
</table>

返回有關與目錄：:ImageSet關聯的影像、視頻、色板以及與URL路徑中指定的影像目錄條目相關的各種元資料的資訊。 該響應是由所提供集合的類型確定的分層結構。 請求「xml」或「json」格式時應用適當的格式。

HTTP響應可以與基於的TTL進行快取 `catalog::NonImgExpiration`。

>[!NOTE]
>
>req=set請求中不允許冒號字元。

支援JSON響應格式的請求允許您使用擴展語法指定JS回調處理程式的名稱 `req=` 參數：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP響應中存在的JS處理程式的名稱。 只允許使用a-z、A-Z和0-9個字元。 選擇性. 預設為 `s7jsonResponse`.
