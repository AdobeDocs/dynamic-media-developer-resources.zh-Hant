---
description: 媒體集資訊。
solution: Experience Manager
title: 設定
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bc69f094-ff21-4dd7-9e10-daddb3de0c65
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 1%

---

# 設定{#set}

媒體集資訊。

req=set[，xml[， *`encoding`*]|{json[&amp;id=*`reqId`*]]

<table id="simpletable_02C955F4EBAD4251A728F0FC68F432B5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">編碼</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> reqId</span> </p></td> 
  <td class="stentry"> <p>唯一請求識別碼 </p></td> 
 </tr> 
</table>

針對URL路徑中指定的影像目錄專案，傳回影像、影片、色票和與catalog：：ImageSet相關聯的各種中繼資料的相關資訊。 此回應為階層式結構，由提供的集合型別決定。 要求&#39;xml&#39;或&#39;json&#39;格式時，會套用適當的格式。

HTTP回應可使用以`catalog::NonImgExpiration`為基礎的TTL進行快取。

>[!NOTE]
>
>req=set要求中不允許使用冒號字元。

支援JSON回應格式的請求可讓您使用`req=`引數的延伸語法來指定JS回呼處理常式的名稱：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`是JSONP回應中存在的JS處理常式名稱。 僅允許a-z、A-Z和0-9字元。 選填。 預設值為`s7jsonResponse`。
