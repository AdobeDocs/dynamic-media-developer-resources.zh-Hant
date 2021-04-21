---
description: 來源影像屬性。 傳回URL路徑中指定之影像檔案或目錄項目的選取屬性。
solution: Experience Manager
title: imageprops
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 7%

---


# imageprops{#imageprops}

來源影像屬性。 傳回URL路徑中指定之影像檔案或目錄項目的選取屬性。

`req=imageprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8E03127D50444CA7878A6B08E866EE2E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>唯一的請求識別碼。 </p></td> 
 </tr> 
</table>

HTTP響應基於`attribute::NonImgExpiration`可以與TTL進行快取。

請求字串中的其他命令會被忽略。

支援JSONP回應格式的請求可讓您使用`req=`參數的擴充語法來指定JS回呼處理常式的名稱：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JS回應中顯示的JS處理常式名稱。僅允許a-z、A-Z和0-9字元。 選填。預設為 `s7jsonResponse`.

傳回下列屬性：

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
   <td> <p> <span class="codeph"> 目錄：:</span> 錨點 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.expiration</span> </p> </td> 
   <td> <p> 雙 </p> </td> 
   <td> <p> <span class="codeph"> 目錄：:</span> 到期或預設存留時間 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p>完整解析度影像高度（像素） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 與此映像關聯的配置檔案的名稱／說明 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 影像. embeddedIccProfile</span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1，如果關聯的描述檔內嵌在影像中 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.embedded PhotoshopPaths</span> </p> </td> 
   <td> <p> 布林值 </p> </td> 
   <td> <p> 1如果影像包含Photoshop路徑資料 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 影像. embeddedXmpData</span> </p> </td> 
   <td> <p> 布林值 </p> </td> 
   <td> <p> 1如果影像包含資XMP料 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask</span> </p> </td> 
   <td> <p> 列舉 </p> </td> 
   <td> <p> 0代表無遮色片，1代表預乘α,2代表非預乘α,3代表個別遮色片影像 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.modifier</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> <span class="codeph"> 目錄：:</span> 修改器或空（如果不是目錄條目） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 影像. photoshopPathNames</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 與此映像關聯的所有Photoshop路徑名稱的逗號分隔清單 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixTyp</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 影像類型可能是「CMYK」、「RGB」或「BW」（對於灰階影像） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.postModifier</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> <span class="codeph"> 屬性：:</span> PostModifieror空（如果不是目錄條目） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes</span> </p> </td> 
   <td> <p> 真實 </p> </td> 
   <td> <p> 預設列印解析度（像素／英吋） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.resolution</span> </p> </td> 
   <td> <p> 真實 </p> </td> 
   <td> <p> <span class="codeph"> 目錄：:</span> Resolution或預設對象解析度 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.timeStamp</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p>修改日期／時間（來自<span class="codeph">目錄：:TimeStamp</span>或影像檔） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbRes</span> </p> </td> 
   <td> <p> 真實 </p> </td> 
   <td> <p> <span class="codeph"> catalog::</span> ThumbResor the default thumbnail resolution </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbType</span> </p> </td> 
   <td> <p> 列舉 </p> </td> 
   <td> <p> <span class="codeph"> catalog::</span> ThumbType或預設縮圖類型 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width</span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p> 完整解析度影像寬度（像素） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.translatedId</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 路徑中指定的<span class="varname">對象</span>已解析到的目錄ID（請參見<a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414" type="reference" format="dita" scope="local">對象ID轉換</a>）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

