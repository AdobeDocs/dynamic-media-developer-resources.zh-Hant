---
description: 響應資料屬性。 評估當前請求時，如果它是映像請求(req=img)，則伺服器不返回映像，而是返回回復映像的選定屬性。
solution: Experience Manager
title: props
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9933d1dc-ae16-4d17-80ca-a1068cd73b0c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 8%

---

# props{#props}

響應資料屬性。 評估當前請求時，如果它是映像請求(req=img)，則伺服器不返回映像，而是返回回復映像的選定屬性。

` req=props[,text|javascript|xml|{json[&id= *`reqId`*}]`

<table id="simpletable_A9FCC880171B4A9DBAE28413AFDF75F7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> reqId </span> </span> </p> </td> 
  <td class="stentry"> <p>唯一請求標識符。 </p> </td> 
 </tr> 
</table>

支援JSONP響應格式的請求允許您使用擴展語法指定JS回調處理程式的名稱 `req=` 參數：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP響應中存在的JS處理程式的名稱。 只允許使用a-z、A-Z和0-9個字元。 選擇性. 預設為 `s7jsonResponse`.

請參閱 [屬性](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9) 的子菜單。 HTTP響應可通過基於的TTL快取 `attribute::NonImgExpiration`。

為/is/image請求返回以下屬性：

<table id="table_9665612ED7D24C07AAF75D953C0FEB36"> 
 <tbody> 
  <tr> 
   <td> <b> 屬性</b> </td> 
   <td> <b> 類型</b> </td> 
   <td> <b> 說明</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 影像.bgc </span> </p> </td> 
   <td> <p> 十六進位 </p> </td> 
   <td> <p> 背景顏色(請參閱 <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88" type="reference" format="dita" scope="local"> bgc= </a> </span>。) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td valign="top"> <p> <span class="codeph"> 影像.height </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> 答復影像高度（以像素為單位） </p> </td> 
  </tr> 
  <tr> 
   <td valign="top"> <p> <span class="codeph"> image.iccEmbed </span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 如果ICC配置檔案嵌入回復影像中，則為True。 (請參閱 <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e" type="reference" format="dita" scope="local"> IccEmbed= </a> </span>。) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.icc配置檔案 </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 與回復影像關聯的配置檔案的名稱/說明。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.length </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> 回復大小（以不包括HTTP頭的像素為單位）;如果伺服器以前未快取回復影像資料，則為0。 (請參閱 <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req=loadcache </a> </span>。) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.mask </span> </p> </td> 
   <td> <p> 枚舉 </p> </td> 
   <td> <p> 如果應答影像包括alpha通道，則1，否則0。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pixTyp </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 回復影像類型，可能 <span class="codeph"> CMYK </span>。 <span class="codeph"> RGB </span> 或 <span class="codeph"> BW </span> （對於灰度影像）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pathEmbed </span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 如果響應影像嵌入了任何路徑，則為1，否則為0。 (請參閱 <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>。) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td> <p> 真實 </p> </td> 
   <td> <p> 打印解析度(dpi) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 影像質量 </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> JPEG質量。 (請參閱 <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352" type="reference" format="dita" scope="local"> qlt= </a> </span>。) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.type </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 回復影像的Mime類型。 (請參閱 <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a" type="reference" format="dita" scope="local"> fmt= </a> </span>。) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> 答復影像寬度（以像素為單位）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.xmpEmbed </span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 如果響應影像嵌入了xmp資料，則為1，否則為0。 (請參閱 <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-xmpembed.md#reference-46ecf40a40a0442fa62de3a85dcb03e8" type="reference" format="dita" scope="local"> xmpEmbed= </a> </span>。) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.version </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 映像版本標識符。 (請參閱 <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id= </a> </span>。) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 元資料。版本 </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 元資料版本標識符。 (請參閱 <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id= </a> </span>。) </p> </td> 
  </tr> 
 </tbody> 
</table>

返回以下屬性 `/is/content` 請求：

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
   <td> <p>部分解析的檔案路徑。 (請參閱 <span class="codeph"> 靜態：：路徑 </span>。) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 長度 </span> </p> </td> 
   <td> <p> 整 </p> </td> 
   <td> <p> 對象檔案大小（以位元組為單位） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 過期 </span> </p> </td> 
   <td> <p> 雙 </p> </td> 
   <td> <p> <span class="codeph"> 靜態：：到期 </span> 或預設生存時間 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 上次修改時間 </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 修改日期/時間(自 <span class="codeph"> 靜態：:TimeStamp </span> 或對象檔案) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> userType </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> <span class="codeph"> 靜態：:UserType </span> </p> </td> 
  </tr> 
 </tbody> 
</table>
