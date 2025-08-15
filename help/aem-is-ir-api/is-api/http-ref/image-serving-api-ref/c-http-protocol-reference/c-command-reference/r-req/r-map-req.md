---
title: 地圖
description: 影像地圖資料。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# 地圖{#map}

影像地圖資料。

`req=map[,text|{xml[, *`編碼`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname">編碼</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>唯一要求識別碼。 </p></td> 
 </tr> 
</table>

查詢未指定其他命令的簡單目錄專案時，傳回`catalog::Map`而不進行修改（不會縮放至`catalog::maxPix`）。

如果在要求中指定了任何其他命令，則會傳回複合影像對應。 複合影像地圖是透過縮放、裁切、旋轉及分層要求中所包含的所有`catalog::Map`及/或`map=`命令所衍生，就像影像資料會與`req=img`一樣。

指定`text`或省略第二個引數，以便您可以傳回回應MIME型別為`HTML <AREA>`的`text/plain`元素字串形式的影像地圖資料。

指定`xml`，讓您可以將回應格式化為XML，而非HTML。 可選擇指定文字編碼。 預設值為`UTF-8`。

如果指定的目錄物件找不到對應資料，和/或在裁切影像後沒有`<AREA>`元素，則傳回空字串（或空的`<AREA>`元素）。

HTTP回應可使用以`catalog::Expiration`為基礎的TTL進行快取。

支援JSONP回應格式的請求可讓您使用`req=`引數的延伸語法來指定JS回呼處理常式的名稱：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`是JSONP回應中出現的JS處理常式名稱。 僅允許a-z、A-Z和0-9字元。 選填。 預設值為`s7jsonResponse`。

檢視[影像地圖](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)。
