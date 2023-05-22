---
description: 映像目錄屬性。 返回在請求路徑中指定的映像目錄的公用屬性。
solution: Experience Manager
title: 編目道具
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 28bf68e8-d424-418e-99a7-5298a1d83341
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 6%

---

# 編目道具{#catalogprops}

映像目錄屬性。 返回在請求路徑中指定的映像目錄的公用屬性。

`req=catalogprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_D1D9183C08834005B482B103CEF2EDA9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>唯一請求標識符。 </p></td> 
 </tr> 
</table>

檢索預設目錄屬性( [!DNL default.ini])，忽略目錄ID。 HTTP響應可以與基於的TTL進行快取 `attribute::NonImgExpiration`。

支援JSONP響應格式的請求允許您使用擴展語法指定JS回調處理程式的名稱 `req=` 參數：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP響應中存在的JS處理程式的名稱。 只允許使用a-z、A-Z和0-9個字元。 選擇性. 預設為 `s7jsonResponse`.

返回以下屬性值：

<table id="table_DEC26CBF274945298BA81B5E2E2F331D"> 
 <tbody> 
  <tr> 
   <td> <b> 屬性</b> </td> 
   <td> <b> 類型</b> </td> 
   <td> <b> 對應的目錄屬性</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.bkg顏色</span> </p> </td> 
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
   <td> <p> <span class="codeph"> catalog.default到期</span> </p> </td> 
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
   <td> <p> <span class="codeph"> 屬性：:LastModified</span>，或，如果不存在，則 <span class="varname"> 目錄</span><span class="filepath"> .ini</span> 檔案 </p> </td> 
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
   <td> <p> 整 </p> </td> 
   <td> <p> <span class="codeph"> 屬性：:PrintResolution</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.publishInfo</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> <span class="codeph"> 屬性：:PublishInfo</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.resMode</span> </p> </td> 
   <td> <p> 枚舉 </p> </td> 
   <td> <p> <span class="codeph"> 屬性：:ResMode</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.resolution</span> </p> </td> 
   <td> <p> 真實 </p> </td> 
   <td> <p> <span class="codeph"> 屬性：：解析度</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbKgColor</span> </p> </td> 
   <td> <p> 十六進位 </p> </td> 
   <td> <p> <span class="codeph"> 屬性：:ThumbBkgColor</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbHorizAlign</span> </p> </td> 
   <td> <p> 枚舉 </p> </td> 
   <td> <p> <span class="codeph"> 屬性：:ThumbHorizAlign</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbRes</span> </p> </td> 
   <td> <p> 真實 </p> </td> 
   <td> <p> <span class="codeph"> 屬性：:ThumbRes</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbType</span> </p> </td> 
   <td> <p> 枚舉 </p> </td> 
   <td> <p> <span class="codeph"> 屬性：:ThumbType</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbVertAlign</span> </p> </td> 
   <td> <p> 枚舉 </p> </td> 
   <td> <p> <span class="codeph"> 屬性：:ThumbVertAlign</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：水印</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> <span class="codeph"> 屬性：：水印</span> </p> </td> 
  </tr> 
 </tbody> 
</table>
