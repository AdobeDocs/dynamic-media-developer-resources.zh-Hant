---
description: 影像映射資料。
solution: Experience Manager
title: 地圖
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 4%

---

# 地圖{#map}

影像映射資料。

`req=map[,text|{xml[, *`編碼`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 編碼</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>唯一請求標識符。 </p></td> 
 </tr> 
</table>

返回 `catalog::Map` 在查詢沒有指定其他命令的簡單目錄條目時不進行修改(將不會縮放到 `catalog::maxPix`)。

如果在請求中指定了任何其他命令，則返回複合影像映射，該映射通過縮放、裁剪、旋轉和分層所有 `catalog::Map` 和/或 `map=` 命令，與影像資料 `req=img`。

指定 `text` 或省略第二個參數以 `HTML <AREA>` 具有響應MIME類型的元素字串 `text/plain`。

指定 `xml` 將響應格式化為XML，而不是HTML。 可選地指定文本編碼。 預設值為 `UTF-8`.

返回空字串(或空 `<AREA>` 元素)，如果找不到指定目錄對象的映射資料，和/或 `<AREA>` 剪切影像後，元素將保留。

HTTP響應可以與基於的TTL進行快取 `catalog::Expiration`。

支援JSONP響應格式的請求允許您使用擴展語法指定JS回調處理程式的名稱 `req=` 參數：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP響應中存在的JS處理程式的名稱。 只允許使用a-z、A-Z和0-9個字元。 選擇性. 預設為 `s7jsonResponse`.

請參閱 [影像映射](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)。
