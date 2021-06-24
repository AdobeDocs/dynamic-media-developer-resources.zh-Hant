---
description: 源映像屬性。 傳回URL路徑中指定之影像檔案或目錄項目的選取屬性。
solution: Experience Manager
title: imageprops
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: b4337c20-8e47-4d61-b234-19434f5c5216
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 7%

---

# imageprops{#imageprops}

源映像屬性。 傳回URL路徑中指定之影像檔案或目錄項目的選取屬性。

`req=imageprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8E03127D50444CA7878A6B08E866EE2E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>唯一請求識別碼。 </p></td> 
 </tr> 
</table>

HTTP回應可根據`attribute::NonImgExpiration`與TTL快取。

請求字串中的其他命令會遭忽略。

支援JSONP回應格式的要求可讓您使用`req=`參數的延伸語法來指定JS回呼處理常式的名稱：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP回應中出現的JS處理常式的名稱。僅允許a-z、A-Z和0-9個字元。 選填。預設為 `s7jsonResponse`.

會傳回下列屬性：

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
   <td> <p> <span class="codeph"> 目錄：:</span> 錨點或預設錨點 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.expiration</span> </p> </td> 
   <td> <p> 雙 </p> </td> 
   <td> <p> <span class="codeph"> 目錄： </span> 過期或預設存留時間 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p>全解析度影像高度（像素） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 與此影像關聯的配置檔案的名稱/說明 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 影像. embeddedIccProfile</span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1如果關聯的配置檔案嵌入到影像中 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.embedded PhotoshopPaths</span> </p> </td> 
   <td> <p> 布林值 </p> </td> 
   <td> <p> 1如果影像包含Photoshop路徑資料 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 影像. embeddedXmpData</span> </p> </td> 
   <td> <p> 布林值 </p> </td> 
   <td> <p> 1如果影像包含XMP資料 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask</span> </p> </td> 
   <td> <p> 列舉 </p> </td> 
   <td> <p> 無遮罩為0，預乘α為1，非預乘α為2，獨立遮罩影像為3 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.modifier</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> <span class="codeph"> 目錄：:</span> 若沒有目錄項目，則修改器為空 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 影像. photoshopPathNames</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 與此影像相關聯的所有Photoshop路徑名稱清單（以逗號分隔） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixTyp</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 影像類型，可以是「CMYK」、「RGB」或「BW」（對於灰度影像） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.postModifier</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> <span class="codeph"> 屬性：:</span> 如果沒有目錄項目，則為空白 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes</span> </p> </td> 
   <td> <p> 真實 </p> </td> 
   <td> <p> 預設打印解析度（像素/英吋） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.resolution</span> </p> </td> 
   <td> <p> 真實 </p> </td> 
   <td> <p> <span class="codeph"> 目錄：:</span> 解析度或預設對象解析度 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.timeStamp</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p>修改日期/時間（來自<span class="codeph">目錄：:TimeStamp</span>或影像檔案） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbRes</span> </p> </td> 
   <td> <p> 真實 </p> </td> 
   <td> <p> <span class="codeph"> 目錄：:</span> 縮圖解析度 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbType</span> </p> </td> 
   <td> <p> 列舉 </p> </td> 
   <td> <p> <span class="codeph"> 目錄：: </span> ThumbType或預設縮圖類型 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width</span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p> 全解析度影像寬度（像素） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.translatedId</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 將路徑中指定的<span class="varname">對象</span>解析到的目錄ID（請參閱<a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414" type="reference" format="dita" scope="local">對象ID轉換</a>）。 </p> </td> 
  </tr> 
 </tbody> 
</table>
