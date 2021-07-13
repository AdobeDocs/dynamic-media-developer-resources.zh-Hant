---
description: 影像目錄屬性。 傳回請求路徑中指定之影像目錄的通用屬性。
solution: Experience Manager
title: 目錄prop
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 28bf68e8-d424-418e-99a7-5298a1d83341
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 6%

---

# 目錄prop{#catalogprops}

影像目錄屬性。 傳回請求路徑中指定之影像目錄的通用屬性。

`req=catalogprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_D1D9183C08834005B482B103CEF2EDA9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>唯一請求識別碼。 </p></td> 
 </tr> 
</table>

要檢索預設目錄屬性([!DNL default.ini])，請忽略目錄ID。 HTTP回應可根據`attribute::NonImgExpiration`與TTL快取。

支援JSONP回應格式的要求可讓您使用`req=`參數的延伸語法來指定JS回呼處理常式的名稱：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP回應中出現的JS處理常式的名稱。僅允許a-z、A-Z和0-9個字元。 選填。預設為 `s7jsonResponse`.

會傳回下列屬性值：

<table id="table_DEC26CBF274945298BA81B5E2E2F331D"> 
 <tbody> 
  <tr> 
   <td> <b> 屬性</b> </td> 
   <td> <b> 類型</b> </td> 
   <td> <b> 對應的目錄屬性</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.bkgColor</span> </p> </td> 
   <td> <p> 十六進位 </p> </td> 
   <td> <p> <span class="codeph"> 屬性：:BkgColor</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：:defaultExt</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> <span class="codeph"> 屬性：:DefaultExt</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.defaultPix</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> 屬性：:DefaultPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.defaultThumbPix</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> 屬性：:DefaultThumbPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.expiration</span> </p> </td> 
   <td> <p> 真實 </p> </td> 
   <td> <p> <span class="codeph"> 屬性：：過期</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.defaultExpiration</span> </p> </td> 
   <td> <p> 真實 </p> </td> 
   <td> <p> <span class="codeph"> 屬性：:DefaultExpiration</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.nonImgExpiration</span> </p> </td> 
   <td> <p> 真實 </p> </td> 
   <td> <p> <span class="codeph"> 屬性：:NonImgExpiration</span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog.fileTime</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> <span class="codeph"> attribute::LastModified</span>，或目錄的上次修改時間（若不存在） <span class="varname"> </span><span class="filepath"> </span> 。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.jpegQuality</span> </p> </td> 
   <td> <p> int,bool </p> </td> 
   <td> <p> <span class="codeph"> 屬性：:JpegQuality</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.maxPix</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> 屬性：:MaxPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.printResolution</span> </p> </td> 
   <td> <p> int </p> </td> 
   <td> <p> <span class="codeph"> 屬性：:PrintResolution</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.publishInfo</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> <span class="codeph"> 屬性：:PublishInfo</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.resMode</span> </p> </td> 
   <td> <p> 列舉 </p> </td> 
   <td> <p> <span class="codeph"> 屬性：:ResMode</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.resolution</span> </p> </td> 
   <td> <p> 真實 </p> </td> 
   <td> <p> <span class="codeph"> 屬性：：解析度</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbBkgColor</span> </p> </td> 
   <td> <p> 十六進位 </p> </td> 
   <td> <p> <span class="codeph"> 屬性：:ThumbBkgColor</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbHorizAlign</span> </p> </td> 
   <td> <p> 列舉 </p> </td> 
   <td> <p> <span class="codeph"> 屬性：:ThumbHorizAlign</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbRes</span> </p> </td> 
   <td> <p> 真實 </p> </td> 
   <td> <p> <span class="codeph"> 屬性：:ThumbRes</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbType</span> </p> </td> 
   <td> <p> 列舉 </p> </td> 
   <td> <p> <span class="codeph"> 屬性：:ThumbType</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbVertAlign</span> </p> </td> 
   <td> <p> 列舉 </p> </td> 
   <td> <p> <span class="codeph"> 屬性：:ThumbVertAlign</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：浮水印</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> <span class="codeph"> 屬性：：浮水印</span> </p> </td> 
  </tr> 
 </tbody> 
</table>
