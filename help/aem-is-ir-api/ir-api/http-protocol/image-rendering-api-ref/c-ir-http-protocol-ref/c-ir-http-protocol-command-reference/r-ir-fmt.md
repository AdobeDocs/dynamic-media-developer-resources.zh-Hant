---
description: 回覆影像格式。 指定發送到客戶端的影像資料的影像編碼格式以及HTTP響應標頭的相應響應MIME類型。
solution: Experience Manager
title: fmt
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 691c5421-0754-45ce-b454-dd0ceff47a58
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 4%

---

# fmt{#fmt}

回覆影像格式。 指定發送到客戶端的影像資料的影像編碼格式以及HTTP響應標頭的相應響應MIME類型。

` fmt= *``*[,[ *``*][, *`formatpixelTypetiffCompression`*]]`

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
  <td class="stentry"> <p>無損失的PNG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png-alpha </p> </td> 
  <td class="stentry"> <p>具有Alpha通道的無損PNG。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif </p> </td> 
  <td class="stentry"> <p>TIFF. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif-alpha </p> </td> 
  <td class="stentry"> <p>含Alpha通道的TIFF。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf </p> </td> 
  <td class="stentry"> <p>有損JPEG嵌入到Macromedia swf檔案中。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf-alpha </p> </td> 
  <td class="stentry"> <p>有損JPEG和嵌入到Macromediaswf檔案中的減縮壓縮掩碼。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>pdf </p> </td> 
  <td class="stentry"> <p>內嵌於PDF中的影像。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>eps </p> </td> 
  <td class="stentry"> <p>未壓縮的二進位封裝PostScript。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif </p> </td> 
  <td class="stentry"> <p>256色的GIF。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif-alpha </p> </td> 
  <td class="stentry"> <p>255色加上索引鍵色透明度的GIF。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pixelType  </span> </p> </td> 
  <td class="stentry"> <p>rgb </p> </td> 
  <td class="stentry"> <p>返回RGB影像資料。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>灰色 </p> </td> 
  <td class="stentry"> <p>傳回灰階影像資料。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>cmy </p> </td> 
  <td class="stentry"> <p>返回CMYK影像資料。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> tiffCompression  </span> </td> 
  <td class="stentry"> <p>無 </p> </td> 
  <td class="stentry"> <p>未壓縮. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>lzw </p> </td> 
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

*`pixelType`* 在未指定時影響輸 `icc=` 出顏色空間轉換；會套用對應的預設顏 *`pixelType`* 色設定檔。如果禁用顏色管理，則應用天真轉換。 *`pixelType`* 指定時會 `icc=` 忽略，而會決定輸出像素類型。

*`compression`* 只有在將tif、tif-alpha或PDF指定為時，才允許使 *`format`*&#x200B;用。有關這些影像格式支援的壓縮選項，請參閱下表。

`qlt-` 為以下格式設定JPEG編碼選項：JPEG、TIFF（含JPEG壓縮）、PDF（含JPEG壓縮）和SWF檔案。如果`fmt=gif`或`fmt=gif-alpha`，請使用`quantize=`。 有關詳細資訊，請參閱命令說明。 其他格式沒有可設定的選項。

對於所有格式和像素類型，每像素元件返回8位。

下表列出&#x200B;*`format`*&#x200B;和&#x200B;*`pixelType`*&#x200B;的有效組合、相應的HTTP響應MIME類型、是否可嵌入ICC配置檔案（請參見[iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)），以及可以應用哪些格式特定的選項命令。

<table id="table_3461A367632E4B5A8AB578850A439024"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> <span class="varname"> 格式 </span> </p> </th> 
   <th colname="col2" class="entry"> <p> <span class="varname"> pixelType  </span> </p> </th> 
   <th colname="col3" class="entry"> <p>回應MIME類型 </p> </th> 
   <th colname="col4" class="entry"> <p>內嵌ICC設定檔 </p> </th> 
   <th colname="col5" class="entry"> <p>選項 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>jpeg, jpg </p> </td> 
   <td colname="col2"> <p>rgb，灰色， cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <span class="codeph"> qlt=  </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png, png,alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png8、png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色， cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression  </span> </p> <p> <span class="codeph"> （無|lzw|zip|jpeg）, pathEmbed=, qlt  </span> </p> <p>（除非將<span class="varname"> tiffCompression </span>設為'jpeg'，否則會忽略<span class="codeph"> qlt= </span>。） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>swf,swf-alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>否 </p> <p>(Flash Player會忽略嵌入的ICC配置檔案。) </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt=  </span>，屬 <span class="codeph"> 性：:TrustedDomains  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pdf </p> </td> 
   <td colname="col2"> <p>rgb，灰色， cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression  </span> </p> <p> <span class="codeph"> （無|zip|jpeg）,qlt=  </span> </p> <p> （除非將<span class="varname"> tiffCompression </span>設為'jpeg'，否則會忽略<span class="codeph"> qlt= </span>。） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eps </p> </td> 
   <td colname="col2"> <p>rgb，灰色， cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed=  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>gif, gif,alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> <p>（轉換為灰色或rgb後，資料會轉換為浮動視窗。） </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>否 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

指定發送到客戶端的答復影像資料的編碼格式，以及HTTP答復標頭的相應響應MIME類型。

`png-alpha` 傳回未關聯的alpha值（亦即，alpha值不會預乘像素值），而 `tif-alpha`且傳 `swf-alpha` 回相關的alpha值（亦即，alpha值會預先乘以alpha值）。Alpha通道對應於暈映的`req=img`背景掩碼的反面；如果存在`req=object`，則對應於組或對象掩碼。 要在使用嵌套IR請求時應用Alpha，請將具有適當Alpha檔案格式的`fmt=`添加到嵌入的IR請求和主請求。 如果使用`icc=`指定CMYK或灰度ICC配置檔案，則不返回Alpha資料。

## 屬性 {#section-eb12a82c69d84622bcea153dd84d95b3}

可發生在要求中的任何位置。

## 預設 {#section-d2c2af11fa974e1a84e0c6cb7fb646fe}

*`format`* 預設為 `attribute::Format`, *`tiffCompression`* 預設為 `attribute::TiffEncoding`。*`pixelType`* 如果未 `rgb` 指 `icc=` 定，則預設為，否則它與指定ICC配置檔案的像素類型相對應。

## 另請參閱 {#section-c55efc881fc94c70bff91b870e026a7b}

[屬性：:Format](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-format.md#reference-da5207242f1c4f1c8fa4df6027121ff2) ,  [attribute::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50),  [attribute::TiffEncoding](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-tiffencoding.md#reference-a3425191166042d59db766c468857d0e),  [qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd),  [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f),  [pathEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb),  [quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38)
