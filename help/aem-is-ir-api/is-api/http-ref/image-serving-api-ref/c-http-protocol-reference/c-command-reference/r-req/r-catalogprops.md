---
description: 影像目錄屬性。 傳回要求路徑中所指定之影像目錄的一般屬性。
solution: Experience Manager
title: catalogprops
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 28bf68e8-d424-418e-99a7-5298a1d83341
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 4%

---

# catalogprops{#catalogprops}

影像目錄屬性。 傳回要求路徑中所指定之影像目錄的一般屬性。

`req=catalogprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_D1D9183C08834005B482B103CEF2EDA9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>唯一要求識別碼。 </p></td> 
 </tr> 
</table>

若要擷取預設目錄屬性( [!DNL default.ini])，請省略目錄識別碼。 HTTP回應可使用以`attribute::NonImgExpiration`為基礎的TTL進行快取。

支援JSONP回應格式的請求可讓您使用`req=`引數的延伸語法來指定JS回呼處理常式的名稱：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`是JSONP回應中出現的JS處理常式名稱。 僅允許a-z、A-Z和0-9字元。 選填。 預設值為`s7jsonResponse`。

系統會傳回下列屬性值：

<table id="table_DEC26CBF274945298BA81B5E2E2F331D"> 
 <tbody> 
  <tr> 
   <td> <b>屬性</b> </td> 
   <td> <b>型別</b> </td> 
   <td> <b>對應的目錄屬性</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.bkgColor</span> </p> </td> 
   <td> <p> 十六進位 </p> </td> 
   <td> <p> <span class="codeph">屬性：：BkgColor</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">目錄：：defaultExt</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> <span class="codeph">屬性：：DefaultExt</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.defaultPix</span> </p> </td> 
   <td> <p> int，int </p> </td> 
   <td> <p> <span class="codeph">屬性：：DefaultPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.defaultThumbPix</span> </p> </td> 
   <td> <p> int，int </p> </td> 
   <td> <p> <span class="codeph">屬性：：DefaultThumbPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.expiration</span> </p> </td> 
   <td> <p> 真實 </p> </td> 
   <td> <p> <span class="codeph">屬性：：Expiration</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.defaultExpiration</span> </p> </td> 
   <td> <p> 真實 </p> </td> 
   <td> <p> <span class="codeph">屬性：：DefaultExpiration</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.nonImgExpiration</span> </p> </td> 
   <td> <p> 真實 </p> </td> 
   <td> <p> <span class="codeph">屬性：：NonImgExpiration</span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog.fileTime</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> <span class="codeph">屬性：：LastModified</span>，如果沒有，則是<span class="varname">目錄</span><span class="filepath"> .ini</span>檔案的上次修改時間 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.jpegQuality</span> </p> </td> 
   <td> <p> int，bool </p> </td> 
   <td> <p> <span class="codeph">屬性：：JpegQuality</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.maxPix</span> </p> </td> 
   <td> <p> int，int </p> </td> 
   <td> <p> <span class="codeph">屬性：：MaxPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.printResolution</span> </p> </td> 
   <td> <p> int </p> </td> 
   <td> <p> <span class="codeph">屬性：：PrintResolution</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.publishInfo</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> <span class="codeph">屬性：：PublishInfo</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.resMode</span> </p> </td> 
   <td> <p> 列舉 </p> </td> 
   <td> <p> <span class="codeph">屬性：：ResMode</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.resolution</span> </p> </td> 
   <td> <p> 真實 </p> </td> 
   <td> <p> <span class="codeph">屬性：：Resolution</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbBkgColor</span> </p> </td> 
   <td> <p> 十六進位 </p> </td> 
   <td> <p> <span class="codeph">屬性：：ThumbBkgColor</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbHorizAlign</span> </p> </td> 
   <td> <p> 列舉 </p> </td> 
   <td> <p> <span class="codeph">屬性：：ThumbHorizAlign</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbRes</span> </p> </td> 
   <td> <p> 真實 </p> </td> 
   <td> <p> <span class="codeph">屬性：：ThumbRes</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbType</span> </p> </td> 
   <td> <p> 列舉 </p> </td> 
   <td> <p> <span class="codeph">屬性：：ThumbType</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbVertAlign</span> </p> </td> 
   <td> <p> 列舉 </p> </td> 
   <td> <p> <span class="codeph">屬性：：ThumbVertAlign</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">目錄：：浮水印</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> <span class="codeph">屬性：：浮水印</span> </p> </td> 
  </tr> 
 </tbody> 
</table>
