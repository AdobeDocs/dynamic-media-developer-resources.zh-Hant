---
description: 媒體集資訊。
solution: Experience Manager
title: 設定
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: bc69f094-ff21-4dd7-9e10-daddb3de0c65
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 4%

---

# 設定{#set}

媒體集資訊。

req=set[,xml[, *`encoding`*]|{json[&amp;id=*`reqId`*]}

<table id="simpletable_02C955F4EBAD4251A728F0FC68F432B5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 編碼</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> reqId</span> </p></td> 
  <td class="stentry"> <p>唯一請求識別碼 </p></td> 
 </tr> 
</table>

傳回與目錄：:ImageSet相關的影像、視訊、色票和各種中繼資料的相關資訊，這些元資料適用於URL路徑中指定的影像目錄項目。 此響應是由提供的集類型確定的分層結構。 請求「xml」或「json」格式時，會套用適當的格式。

HTTP回應可根據`catalog::NonImgExpiration`與TTL快取。

>[!NOTE]
>
>在req=set請求中不允許冒號字元。

支援JSON回應格式的要求可讓您使用`req=`參數的擴充語法，指定JS回呼處理常式的名稱：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP回應中出現的JS處理常式的名稱。僅允許a-z、A-Z和0-9個字元。 選填。預設為 `s7jsonResponse`.
