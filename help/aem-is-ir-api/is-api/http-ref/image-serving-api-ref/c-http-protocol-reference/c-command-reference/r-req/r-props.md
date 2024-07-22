---
description: 回應資料屬性。 評估目前的請求，就像請求影像一樣(req=img)，但伺服器不會傳回影像，而是傳回回覆影像的選定屬性。
solution: Experience Manager
title: props
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9933d1dc-ae16-4d17-80ca-a1068cd73b0c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 5%

---

# props{#props}

回應資料屬性。 評估目前的請求，就像請求影像一樣(req=img)，但伺服器不會傳回影像，而是傳回回覆影像的選定屬性。

` req=props[,text|javascript|xml|{json[&id= *`reqId`*}]`

<table id="simpletable_A9FCC880171B4A9DBAE28413AFDF75F7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> reqId </span> </span> </p> </td> 
  <td class="stentry"> <p>唯一要求識別碼。 </p> </td> 
 </tr> 
</table>

支援JSONP回應格式的請求可讓您使用`req=`引數的延伸語法來指定JS回呼處理常式的名稱：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`是JSONP回應中出現的JS處理常式名稱。 僅允許a-z、A-Z和0-9字元。 選填。 預設值為`s7jsonResponse`。

如需回覆語法和回應MIME型別的說明，請參閱[屬性](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9)。 可使用以`attribute::NonImgExpiration`為基礎的TTL來快取HTTP回應。

系統會為/is/image要求傳回下列屬性：

<table id="table_9665612ED7D24C07AAF75D953C0FEB36"> 
 <tbody> 
  <tr> 
   <td> <b>屬性</b> </td> 
   <td> <b>型別</b> </td> 
   <td> <b>描述</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.bgc </span> </p> </td> 
   <td> <p> 十六進位 </p> </td> 
   <td> <p> 背景顏色（請參閱<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88" type="reference" format="dita" scope="local"> bgc= </a> </span>。） </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td valign="top"> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> 回覆影像高度（畫素） </p> </td> 
  </tr> 
  <tr> 
   <td valign="top"> <p> <span class="codeph"> image.iccEmbed </span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 如果ICC設定檔已內嵌在回覆影像中，則為True。 （請參閱<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e" type="reference" format="dita" scope="local"> IccEmbed= </a> </span>。） </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 與回覆影像相關聯的設定檔名稱/說明。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.length </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> 回覆大小（以畫素為單位）不包括HTTP標頭；如果伺服器先前未快取回覆影像資料，則為0。 （請參閱<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req=loadcache </a> </span>。） </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.mask </span> </p> </td> 
   <td> <p> 列舉 </p> </td> 
   <td> <p> 如果回覆影像包含Alpha色版，則為1，否則為0。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pixTyp </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 回覆影像型別，可能是<span class="codeph"> CMYK </span>、<span class="codeph">RGB</span>或<span class="codeph"> BW </span> （適用於灰階影像）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pathEmbed </span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 如果回應影像嵌入任何路徑，則為1，否則為0。 （請參閱<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>。） </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td> <p> 真實 </p> </td> 
   <td> <p> 列印解析度(dpi) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.quality </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> JPEG品質。 （請參閱<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352" type="reference" format="dita" scope="local"> qlt= </a> </span>。） </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.type </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 回覆影像的MIME型別。 （請參閱<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a" type="reference" format="dita" scope="local"> fmt= </a> </span>。） </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> 回覆影像寬度（畫素）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.xmpEmbed </span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 如果回應影像嵌入xmp資料，則為1，否則為0。 （請參閱<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-xmpembed.md#reference-46ecf40a40a0442fa62de3a85dcb03e8" type="reference" format="dita" scope="local"> xmpEmbed= </a> </span>。） </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.version </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 影像版本識別碼。 （請參閱<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> ID= </a> </span>。） </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> metadata.version </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 中繼資料版本識別碼。 （請參閱<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> ID= </a> </span>。） </p> </td> 
  </tr> 
 </tbody> 
</table>

為`/is/content`要求傳回下列屬性：

<table id="table_B66360C475CE495D9701AB526E758873"> 
 <tbody> 
  <tr> 
   <td> <b>屬性</b> </td> 
   <td> <b>型別</b> </td> 
   <td> <b>描述</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">路徑</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p>部分解析的檔案路徑。 （請參閱<span class="codeph">靜態：：路徑</span>。） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">長度</span> </p> </td> 
   <td> <p> int </p> </td> 
   <td> <p> 物件檔案大小（位元組） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">到期</span> </p> </td> 
   <td> <p> 雙 </p> </td> 
   <td> <p> <span class="codeph">靜態：：到期</span>或預設存留時間 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> lastModified </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 修改日期/時間（來自<span class="codeph">靜態：：TimeStamp </span>或物件檔案） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">使用者型別</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> <span class="codeph">靜態：：UserType </span> </p> </td> 
  </tr> 
 </tbody> 
</table>
