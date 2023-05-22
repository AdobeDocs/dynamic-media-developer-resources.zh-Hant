---
description: 源影像屬性。 返回在URL路徑中指定的影像檔案或目錄條目的選定屬性。
solution: Experience Manager
title: 影像
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4337c20-8e47-4d61-b234-19434f5c5216
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 7%

---

# 影像{#imageprops}

源影像屬性。 返回在URL路徑中指定的影像檔案或目錄條目的選定屬性。

`req=imageprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8E03127D50444CA7878A6B08E866EE2E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>唯一請求標識符。 </p></td> 
 </tr> 
</table>

HTTP響應可以與基於的TTL進行快取 `attribute::NonImgExpiration`。

請求字串中的其他命令將被忽略。

支援JSONP響應格式的請求允許您使用擴展語法指定JS回調處理程式的名稱 `req=` 參數：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP響應中存在的JS處理程式的名稱。 只允許使用a-z、A-Z和0-9個字元。 選擇性. 預設為 `s7jsonResponse`.

返回以下屬性：

<table id="table_5F289E2E21594A5598DF98E65DEDDFA0"> 
 <tbody> 
  <tr> 
   <td> <b> 屬性</b> </td> 
   <td> <b> 類型</b> </td> 
   <td> <b> 說明</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.anchor</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> 目錄：：錨點</span> 或預設錨點 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.expiration</span> </p> </td> 
   <td> <p> 雙 </p> </td> 
   <td> <p> <span class="codeph"> 目錄：：到期</span> 或預設生存時間 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 影像.height</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p>全解析度影像高度（以像素為單位） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.icc配置檔案</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 與此映像關聯的配置檔案的名稱/說明 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 影像. 嵌入式IccProfile</span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1，如果關聯的配置檔案嵌入到影像中 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.embedded PhotoshopPaths</span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1如果影像包括Photoshop路徑資料 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 影像. 嵌入式XmpData</span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1，如果影像包含數XMP據 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask</span> </p> </td> 
   <td> <p> 枚舉 </p> </td> 
   <td> <p> 0表示無蒙版，1表示預乘α,2表示非預乘α,3表示單獨的蒙版影像 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.modifier</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> <span class="codeph"> 目錄：：修改量</span> 或空（如果不是目錄條目） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 影像. photoshopPathNames</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 與此影像關聯的所有Photoshop路徑的名稱清單（以逗號分隔） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixTyp</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 影像類型，可以是「CMYK」、「RGB」或「BW」（對於灰度影像） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.postModifier</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> <span class="codeph"> 屬性：:PostModifier</span> 或空（如果不是目錄條目） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes</span> </p> </td> 
   <td> <p> 真實 </p> </td> 
   <td> <p> 預設打印解析度（像素/英吋） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.resolution</span> </p> </td> 
   <td> <p> 真實 </p> </td> 
   <td> <p> <span class="codeph"> 目錄：：解析</span> 或預設對象解析度 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.timeStamp</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p>修改日期/時間(自 <span class="codeph"> 目錄：:TimeStamp</span> 或影像檔案) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbRes</span> </p> </td> 
   <td> <p> 真實 </p> </td> 
   <td> <p> <span class="codeph"> 目錄：:ThumbRes</span> 或預設縮略圖解析度 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbType</span> </p> </td> 
   <td> <p> 枚舉 </p> </td> 
   <td> <p> <span class="codeph"> 目錄：:ThumbType</span> 或預設縮略圖類型 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> 全解析度影像寬度（像素） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.translatedId</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 目錄ID <span class="varname"> 對象</span> 已解析路徑中指定的(請參見 <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414" type="reference" format="dita" scope="local"> 對象ID轉換</a>)。 </p> </td> 
  </tr> 
 </tbody> 
</table>
