---
description: 影像目錄屬性。 傳回在請求路徑中指定的影像目錄的通用屬性。
solution: Experience Manager
title: 編目prop
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 6%

---


# catalogprops{#catalogprops}

影像目錄屬性。 傳回在請求路徑中指定的影像目錄的通用屬性。

`req=catalogprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_D1D9183C08834005B482B103CEF2EDA9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>唯一的請求識別碼。 </p></td> 
 </tr> 
</table>

要檢索預設目錄屬性([!DNL default.ini])，請忽略目錄ID。 HTTP響應基於`attribute::NonImgExpiration`可以與TTL進行快取。

支援JSONP回應格式的請求可讓您使用`req=`參數的擴充語法來指定JS回呼處理常式的名稱：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JS回應中顯示的JS處理常式名稱。僅允許a-z、A-Z和0-9字元。 選填。預設為 `s7jsonResponse`.

傳回下列屬性值：

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
   <td> <p> <span class="codeph"> 屬性：：到期</span> </p> </td> 
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
   <td> <p> <span class="codeph"> 屬性：:LastModified</span>，或catalog <span class="varname"> </span><span class="filepath"> .</span> inifile的上次修改時間（如果不存在） </p> </td> 
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
   <td> <p> <span class="codeph"> 屬性：:Watermark</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

