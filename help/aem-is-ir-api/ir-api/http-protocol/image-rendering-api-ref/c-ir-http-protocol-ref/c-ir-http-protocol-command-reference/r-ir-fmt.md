---
title: fm
description: 答復影像格式。 指定發送到客戶端的影像資料的影像編碼格式和HTTP響應標頭的相應響應MIME類型。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 691c5421-0754-45ce-b454-dd0ceff47a58
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 4%

---

# fm {#fmt}

答復影像格式。 指定發送到客戶端的影像資料的影像編碼格式和HTTP響應標頭的相應響應MIME類型。

` fmt= *`格式`*[,[ *`像素類型`*][, *`tiff壓縮`*]]`

<table id="simpletable_200779AA8D8D49A089A295AED5C98C8F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 格式 </span> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>有損JPEG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpg </p> </td> 
  <td class="stentry"> <p>有損JPG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png </p> </td> 
  <td class="stentry"> <p>無損PNG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png-alpha </p> </td> 
  <td class="stentry"> <p>具有Alpha通道的無損PNG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>提 </p> </td> 
  <td class="stentry"> <p>TIFF。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>提夫α </p> </td> 
  <td class="stentry"> <p>TIFF帶α通道。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf </p> </td> 
  <td class="stentry"> <p>有損JPEG嵌入到Macromediaswf檔案中。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf-alpha </p> </td> 
  <td class="stentry"> <p>有損JPEG和嵌入到Macromediaswf檔案中的壓縮掩碼。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>pdf </p> </td> 
  <td class="stentry"> <p>嵌入在PDF中的影像。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>蜂 </p> </td> 
  <td class="stentry"> <p>未壓縮的二進位封裝PostScript。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif </p> </td> 
  <td class="stentry"> <p>GIF有256種顏色。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif-alpha </p> </td> 
  <td class="stentry"> <p>GIF,255色加上鍵色透明度。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 像素類型 </span> </p> </td> 
  <td class="stentry"> <p>rgb </p> </td> 
  <td class="stentry"> <p>返回RGB影像資料。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>灰 </p> </td> 
  <td class="stentry"> <p>返回灰階影像資料。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>色 </p> </td> 
  <td class="stentry"> <p>返回CMYK影像資料。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> tiff壓縮 </span> </td> 
  <td class="stentry"> <p>無 </p> </td> 
  <td class="stentry"> <p>未壓縮。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>洛茲 </p> </td> 
  <td class="stentry"> <p>LZW(Lempel-Ziv-Welch)壓縮（無損）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>郵遞區號 </p> </td> 
  <td class="stentry"> <p>"Deflate"壓縮（無損）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>JPEG壓縮（有損）。 </p> </td> 
 </tr> 
</table>

*`pixelType`* 在 `icc=` 未指定；對應於 *`pixelType`* 的子菜單。 如果禁用顏色管理，則應用天真的轉換。 *`pixelType`* 在 `icc=` 指定，它確定輸出像素類型。

*`compression`* 僅當將tif、tif-alpha或PDF指定為 *`format`*。 有關這些影像格式支援的壓縮選項，請參閱下表。

`qlt-` 設定這些格式的JPEG編碼選項：JPEG、TIFF與JPEG壓縮、PDF與JPEG壓縮以及SWF檔案。 使用 `quantize=` 如果 `fmt=gif` 或 `fmt=gif-alpha`。 有關詳細資訊，請參閱命令說明。 其他格式沒有可設定的選項。

對於所有格式和像素類型，每像素元件返回八位。

下表列出了 *`format`* 和 *`pixelType`*，相應的HTTP響應MIME類型，是否可以嵌入ICC配置檔案(請參見 [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f))，以及可以應用哪些格式特定的選項命令。

<table id="table_3461A367632E4B5A8AB578850A439024"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> <span class="varname"> 格式 </span> </p> </th> 
   <th colname="col2" class="entry"> <p> <span class="varname"> 像素類型 </span> </p> </th> 
   <th colname="col3" class="entry"> <p>響應MIME類型 </p> </th> 
   <th colname="col4" class="entry"> <p>嵌入ICC配置檔案 </p> </th> 
   <th colname="col5" class="entry"> <p>選項 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>jpeg,jpg </p> </td> 
   <td colname="col2"> <p>rgb，灰色，cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <span class="codeph"> qlt= </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png, png,alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png8、png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>tif,tif-α </p> </td> 
   <td colname="col2"> <p>rgb，灰色，cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/tiff&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiff壓縮 </span> </p> <p> <span class="codeph"> (none|lzw|zip|jpeg),pathEmbed=,qlt </span> </p> <p>( <span class="codeph"> qlt= </span> 除非 <span class="varname"> tiff壓縮 </span> 設定為「jpeg」)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>swf,swf,alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-shockwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>否 </p> <p>(該Flash Player忽略嵌入的ICC配置檔案。) </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>。 <span class="codeph"> 屬性：:TrustedDomains </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pdf </p> </td> 
   <td colname="col2"> <p>rgb，灰色，cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiff壓縮 </span> </p> <p> <span class="codeph"> （無|zip|jpeg）,qlt= </span> </p> <p> ( <span class="codeph"> qlt= </span> 除非 <span class="varname"> tiff壓縮 </span> 設定為「jpeg」)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>蜂 </p> </td> 
   <td colname="col2"> <p>rgb，灰色，cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/eps&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>gif, gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> <p>（資料在轉換為灰色或rgb後轉換為調色板。） </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>否 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

指定發送到客戶端的答復影像資料的編碼格式和HTTP答復標頭的相應響應MIME類型。

`png-alpha` 返回未關聯的Alpha（即，Alpha不會預乘像素值），而 `tif-alpha`, `swf-alpha` 返回關聯的alpha（即，alpha值與alpha值預乘）。 該α通道對應於視頻的背景掩模的逆 `req=img`，如果存在 `req=object`。 要在使用嵌套IR請求時應用Alpha，請添加 `fmt=` 嵌入式IR請求和主請求的Alpha檔案格式。 如果使用指定CMYK或灰度ICC配置檔案，則不返回Alpha資料 `icc=`。

## 屬性 {#section-eb12a82c69d84622bcea153dd84d95b3}

可以在請求中的任何位置發生。

## 預設 {#section-d2c2af11fa974e1a84e0c6cb7fb646fe}

*`format`* 預設為 `attribute::Format`和 *`tiffCompression`* 預設值 `attribute::TiffEncoding`。 *`pixelType`* 預設為 `rgb` 如果 `icc=` 未指定，否則它對應於指定ICC配置檔案的像素類型。

## 另請參閱 {#section-c55efc881fc94c70bff91b870e026a7b}

[屬性：：格式](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-format.md#reference-da5207242f1c4f1c8fa4df6027121ff2) 。 [屬性：:JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)。 [屬性：:TiffEncoding](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-tiffencoding.md#reference-a3425191166042d59db766c468857d0e)。 [qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd)。 [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)。 [pathEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f)。 [請求=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)。 [量化=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38)
