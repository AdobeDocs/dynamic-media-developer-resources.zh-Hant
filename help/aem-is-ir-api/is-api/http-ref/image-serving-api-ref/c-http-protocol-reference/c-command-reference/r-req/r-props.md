---
description: 回應資料屬性。 將當前請求評估為影像請求(req=img)，但伺服器不返回影像，而返回回復影像的選定屬性。
solution: Experience Manager
title: props
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9933d1dc-ae16-4d17-80ca-a1068cd73b0c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 8%

---

# prop{#props}

回應資料屬性。 將當前請求評估為影像請求(req=img)，但伺服器不返回影像，而返回回復影像的選定屬性。

` req=props[,text|javascript|xml|{json[&id= *`reqId`*}]`

<table id="simpletable_A9FCC880171B4A9DBAE28413AFDF75F7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> reqId  </span> </span> </p> </td> 
  <td class="stentry"> <p>唯一請求識別碼。 </p> </td> 
 </tr> 
</table>

支援JSONP回應格式的要求可讓您使用`req=`參數的延伸語法來指定JS回呼處理常式的名稱：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP回應中出現的JS處理常式的名稱。僅允許a-z、A-Z和0-9個字元。 選填。預設為 `s7jsonResponse`.

有關回覆語法和回應MIME類型的說明，請參閱[屬性](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9)。 HTTP回應可依據`attribute::NonImgExpiration`以TTL快取。

針對/is/image要求傳回下列屬性：

<table id="table_9665612ED7D24C07AAF75D953C0FEB36"> 
 <tbody> 
  <tr> 
   <td> <b> 屬性</b> </td> 
   <td> <b> 類型</b> </td> 
   <td> <b> 說明</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.bgc  </span> </p> </td> 
   <td> <p> 十六進位 </p> </td> 
   <td> <p> 背景顏色（請參閱<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88" type="reference" format="dita" scope="local"> bgc= </a> </span>。） </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td valign="top"> <p> <span class="codeph"> image.height  </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> 回覆影像高度（像素） </p> </td> 
  </tr> 
  <tr> 
   <td valign="top"> <p> <span class="codeph"> image.iccEmbed  </span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 如果ICC配置檔案嵌入回復影像中，則返回true。 （請參閱<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e" type="reference" format="dita" scope="local"> IccEmbed= </a> </span>。） </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.iccProfile  </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 與回覆影像相關聯的設定檔名稱/說明。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.length  </span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p> 回覆大小（像素），不含HTTP標題；如果伺服器先前未快取回覆影像資料，則為0。 （請參閱<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req=loadcache </a> </span>。） </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.mask  </span> </p> </td> 
   <td> <p> 列舉 </p> </td> 
   <td> <p> 1如果回復影像包括α通道，則0否。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pixTyp  </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 回覆影像類型，可以是<span class="codeph"> CMYK </span>、<span class="codeph"> RGB </span>或<span class="codeph"> BW </span>（對於灰度影像）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pathEmbed  </span> </p> </td> 
   <td> <p> 布林值 </p> </td> 
   <td> <p> 1如果回應影像內嵌任何路徑，否則為0。 （請參閱<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>。） </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.printRes  </span> </p> </td> 
   <td> <p> 真實 </p> </td> 
   <td> <p> 打印解析度(dpi) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.quality  </span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p> JPEG質量。 （請參閱<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352" type="reference" format="dita" scope="local"> qlt= </a> </span>。） </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.type  </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 回覆影像的MIME類型。 （請參閱<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a" type="reference" format="dita" scope="local"> fmt= </a> </span>。） </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.width  </span> </p> </td> 
   <td> <p> 整數 </p> </td> 
   <td> <p> 回覆影像寬度（像素）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.xmpEmbed  </span> </p> </td> 
   <td> <p> 布林值 </p> </td> 
   <td> <p> 1如果回應影像內嵌xmp資料，否則為0。 （請參閱<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-xmpembed.md#reference-46ecf40a40a0442fa62de3a85dcb03e8" type="reference" format="dita" scope="local"> xmpEmbed= </a> </span>。） </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.version  </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 影像版本識別碼。 （請參閱<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id= </a> </span>。） </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> metadata.version  </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 中繼資料版本識別碼。 （請參閱<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id= </a> </span>。） </p> </td> 
  </tr> 
 </tbody> 
</table>

針對`/is/content`請求傳回下列屬性：

<table id="table_B66360C475CE495D9701AB526E758873"> 
 <tbody> 
  <tr> 
   <td> <b> 屬性</b> </td> 
   <td> <b> 類型</b> </td> 
   <td> <b> 說明</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 路徑 </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p>部分解析的檔案路徑。 （請參閱<span class="codeph">靜態：：路徑</span>。） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 長度 </span> </p> </td> 
   <td> <p> int </p> </td> 
   <td> <p> 對象檔案大小（以位元組為單位） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 過期 </span> </p> </td> 
   <td> <p> 雙 </p> </td> 
   <td> <p> <span class="codeph"> static:：過期 </span> 或預設存留時間 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> lastModified  </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 修改日期/時間（來自<span class="codeph">靜態：:TimeStamp </span>或對象檔案） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> userType  </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> <span class="codeph"> static::UserType  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>
