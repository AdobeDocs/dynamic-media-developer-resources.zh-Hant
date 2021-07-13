---
description: 影像地圖資料。
solution: Experience Manager
title: 地圖
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 4%

---

# 地圖{#map}

影像地圖資料。

`req=map[,text|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 編碼</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>唯一請求識別碼。 </p></td> 
 </tr> 
</table>

在查詢沒有指定其他命令的簡單目錄條目時（將不縮放為`catalog::maxPix`），返回`catalog::Map`，而不進行修改。

如果請求中指定了任何其他命令，則會傳回複合影像映射，該映射是透過縮放、裁切、旋轉和分層請求中包含的所有`catalog::Map`和/或`map=`命令而衍生，就像影像資料會包含`req=img`一樣。

指定`text`或忽略第二個參數，以`HTML <AREA>`元素字串的形式傳回影像映射資料，回應MIME類型`text/plain`。

指定`xml`以將回應格式化為XML而非HTML。 可選擇指定文字編碼。 預設值為 `UTF-8`.

如果沒有找到指定目錄對象的映射資料，和/或在裁切影像後沒有保留任何`<AREA>`元素，則返回空字串（或空`<AREA>`元素）。

HTTP回應可根據`catalog::Expiration`與TTL快取。

支援JSONP回應格式的要求可讓您使用`req=`參數的延伸語法來指定JS回呼處理常式的名稱：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP回應中出現的JS處理常式的名稱。僅允許a-z、A-Z和0-9個字元。 選填。預設為 `s7jsonResponse`.

請參閱[影像地圖](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)。
