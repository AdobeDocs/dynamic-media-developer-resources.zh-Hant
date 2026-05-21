---
description: 媒體集資訊。
solution: Experience Manager
title: 設定
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bc69f094-ff21-4dd7-9e10-daddb3de0c65
TQID: 'https://experienceleague.adobe.com/nfNdFeRk7TDhSYHdy05x6fxNKMBhTF7f11xoji13VP4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 144
ht-degree: 2%

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

`<reqHandler>`是JSONP回應中存在的JS處理常式名稱。 僅允許a-z、A-Z和0-9字元。 選擇性. 預設值為`s7jsonResponse`。
