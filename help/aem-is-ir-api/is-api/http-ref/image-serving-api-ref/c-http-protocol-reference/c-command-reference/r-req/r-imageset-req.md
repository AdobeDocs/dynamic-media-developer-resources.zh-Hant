---
description: 影像目錄中的影像集資料。 返回在URL路徑中指定的影像目錄條目的影像集資料。
solution: Experience Manager
title: 映像集
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: 730e7db9-47f0-4e96-8948-18b8185a5b7a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 2%

---

# 映像集{#imageset}

影像目錄中的影像集資料。 返回在URL路徑中指定的影像目錄條目的影像集資料。

`req=imageset[,text|javascript|{xml[, *`編碼`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 編碼</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 請求ID</span></span> </p></td> 
  <td class="stentry"> <p>唯一請求標識符。 </p></td> 
 </tr> 
</table>

內容 `catalog::ImageSet` 返回，但不作進一步修改（如果適用，除外字串本地化），然後是單行終結器(CR/LF)。 如果URL路徑未解析為有效的目錄條目，則響應僅由單行終結器組成。

請求字串中的其他命令將被忽略。 HTTP響應可以與基於的TTL進行快取 `catalog::NonImgExpiration`。

支援JSONP響應格式的請求允許您使用擴展語法指定JS回調處理程式的名稱 `req=` 參數：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP響應中存在的JS處理程式的名稱。 只允許使用a-z、A-Z和0-9個字元。 選擇性. 預設為 `s7jsonResponse`.
