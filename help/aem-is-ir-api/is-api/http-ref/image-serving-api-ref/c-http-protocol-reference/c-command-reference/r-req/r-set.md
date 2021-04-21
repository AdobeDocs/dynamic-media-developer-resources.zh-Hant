---
description: 媒體設定資訊。
solution: Experience Manager
title: 設定
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 4%

---


# 設定{#set}

媒體設定資訊。

req=set[,xml[, *`encoding`*]|{json[&amp;id=*`reqId`*]}]

<table id="simpletable_02C955F4EBAD4251A728F0FC68F432B5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 編碼</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> reqId</span> </p></td> 
  <td class="stentry"> <p>唯一的請求識別碼 </p></td> 
 </tr> 
</table>

傳回與目錄：:ImageSet相關的影像、視訊、色票和各種中繼資料，以取得URL路徑中指定之影像目錄項目的相關資訊。 該響應是由提供的集合類型確定的分層結構。 請求「xml」或「json」格式時，會套用適當的格式。

HTTP響應基於`catalog::NonImgExpiration`可以與TTL進行快取。

>[!NOTE]
>
>req=set請求中不允許冒號字元。

支援JSON回應格式的請求可讓您使用`req=`參數的擴充語法來指定JS回呼處理常式的名稱：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP回應中顯示的JS處理常式名稱。僅允許a-z、A-Z和0-9字元。 選填。預設為 `s7jsonResponse`.
