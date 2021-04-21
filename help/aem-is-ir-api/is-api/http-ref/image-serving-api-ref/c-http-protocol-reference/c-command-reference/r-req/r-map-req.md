---
description: 影像地圖資料。
solution: Experience Manager
title: 地圖
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 4%

---


# 地圖{#map}

影像地圖資料。

`req=map[,text|{xml[, *`EncodingreqId`*]}|{json[&id= *``*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 編碼</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>唯一的請求識別碼。 </p></td> 
 </tr> 
</table>

在查詢沒有指定其他命令的簡單目錄條目時返回`catalog::Map`（不會縮放為`catalog::maxPix`），但不進行修改。

如果請求中指定了任何其他命令，則會傳回合成影像地圖，其衍生方式是縮放、裁切、旋轉和分層請求中包含的所有`catalog::Map`和／或`map=`命令，就像影像資料與`req=img`一樣。

指定`text`或省略第二個參數，以`HTML <AREA>`元素字串形式傳回影像地圖資料，回應MIME類型`text/plain`。

指定`xml`將回應格式設為XML，而非HTML。 可選擇指定文字編碼。 預設值為 `UTF-8`.

如果找不到指定目錄物件的對應資料，且／或在裁切影像後沒有保留`<AREA>`元素，則傳回空字串（或空的`<AREA>`元素）。

HTTP響應基於`catalog::Expiration`可以與TTL進行快取。

支援JSONP回應格式的請求可讓您使用`req=`參數的擴充語法來指定JS回呼處理常式的名稱：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JS回應中顯示的JS處理常式名稱。僅允許a-z、A-Z和0-9字元。 選填。預設為 `s7jsonResponse`.

請參閱[影像地圖](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)。
