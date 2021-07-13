---
description: 回應影像格式。
solution: Experience Manager
title: fmt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67f8a58d-88f5-4993-9749-41a3c530adba
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '916'
ht-degree: 4%

---

# fmt{#fmt}

回應影像格式。

`fmt=format[,` `[`*`pixelType`*`]`,`[`*`compression`*`]]`

*`format`* - avif-alpha | avif | eps | f4m | gif-alpha | gif | jpeg | jpeg2000-alpha | jpeg2000 | jpegxr-alpha | jpegxr | jpg | m3u8 | pdf | pjpeg | png-alpha | png | png8-alpha | png8 |swf-alpha |swf | swf3-alpha | swf3 | tif-alpha | tif | web-alpha | webp

| *`format`* | 說明 |
|---|---|
| `avif-alpha` | 具有Alpha通道&#x200B;<br><br>*的有損和無損AVIF，此格式的發行時間表：* <br><b>北美</b> — 現已提供<br><b>歐洲、中東、非洲</b> - 2021年8月13日<br><b>亞太</b> — 現已提供 |
| `avif` | 有損和無損的AVIF <br><br>*此格式的發行時間表：*<br><b>&#x200B;北美</b> — 現已提供<br><b>歐洲、中東、非洲</b> - 2021年8月13日<br><b>亞太</b> — 現已提供 |
| `eps` | 未壓縮的二進位封裝PostScript |
| `f4m` | Flash串流伺服器資訊清單格式 |
| `gif-alpha` | 2到255色的GIF加上索引鍵色透明度 |
| `gif` | 2到256色的GIF |
| `jpeg` | 有損JPEG |
| `jpeg2000-alpha` | 帶Alpha通道的有損和無損JPEG 2000 |
| `jpeg2000` | 有損和無損JPEG 2000 |
| `jpegxr-alpha` | 具有Alpha通道的有損和無損JPEG XR |
| `jpegxr` | 有損和無損JPEG XR |
| `jpg` | 有損JPG |
| `m3u8` | Apple串流伺服器資訊清單格式 |
| `pdf` | 內嵌於PDF中的影像 |
| `pjpeg` | 漸進式 JPEG 圖像 |
| `png-alpha` | 帶Alpha通道的24位無損PNG |
| `png` | 24位無損PNG |
| `png8-alpha` | 帶Alpha通道的8位無損PNG |
| `png8` | 8位無損PNG |
| `swf-alpha` | 有損JPEG和嵌入到AdobeAS2swf檔案的減縮壓縮掩碼 |
| `swf` | 嵌入到AdobeAS2swf檔案中的有損JPEG |
| `swf3-alpha` | 有損JPEG和嵌入到AdobeAS3swf檔案中的減縮壓縮掩碼。 **注意：** 最適合ActionScript2應用程式(Flash Player8及更舊版本)的swf和swf-alpha格式。建議將swf3和swf3-alpha格式用於ActionScript3應用程式(Flash Player9和更新版本) |
| `swf3` | 有損JPEG嵌入到AdobeAS3swf檔案中 |
| `tif-alpha` | 含Alpha通道的TIFF |
| `tif` | TIFF |
| `webp-alpha` | 帶Alpha通道的有損和無損WebP |
| `webp` | 有損和無損WebP |

| *`pixelType`* – rgb | 灰色 | cmy |
| *`pixelType`* | 說明 |
|---|---|
| `cmyk` | 返回CMYK影像資料。 |
| `gray` | 傳回灰階影像資料。 |
| `rgb` | 返回RGB影像資料。 |

| *`compression`* – none | lzw | 郵遞區號 | jpeg | 有損 | 無損 |
| *`compression`* | 說明 |
|---|---|
| `jpeg` | JPEG壓縮（有損） |
| `lossy` | WebP、JPEG 2000和JPEG XR壓縮（有損） |
| `lossless` | WebP、JPEG 2000和JPEG XR壓縮（無損） |
| `lzw` | LZW(Lempel-Ziv-Welch)壓縮（無損） |
| `none` | 未壓縮 |
| `zip` | &quot;Deflate&quot;壓縮（無損） |

* *`format`* 指定發送到客戶端的影像資料的影像編碼格式以及HTTP響應標頭的相應響應MIME類型。
* *`pixelType`* 可用於在未指定時實現輸出色 `icc=` 域轉換。

   會套用與&#x200B;*`pixelType`*&#x200B;對應的預設顏色設定檔。 如果禁用顏色管理，則應用天真轉換。 *`pixelType`* 指定時會 `icc=` 忽略，而會決定輸出像素類型。

* *`compression`* 只有在將 `tif`、  `tif-alpha`、  `pdf`、  `webp`、  `webp-alpha`、  `jpeg2000`、  `jpeg2000-alpha`、  `jpegxr`或 `jpegxr-alpha` 指定為 *`format`*&#x200B;時，才允許使用。有關這些影像格式支援的壓縮選項，請參閱下表。

您可以使用`qlt=`來設定這些格式的JPEG編碼選項：JPEG、TIFF（含JPEG壓縮）、PDF（含JPEG壓縮）和SWF。 WebP、JPEG 2000和JPEG XR也使用`qlt=`，但這些值會導致不同格式的不同品質。 如果`fmt=gif`或`fmt=gif-alpha`，請使用`quantize=`。 有關詳細資訊，請參閱命令說明。 其他格式沒有可設定的選項。

所有&#x200B;*`formats`*&#x200B;和&#x200B;*`pixelTypes`*&#x200B;都返回每像素8位元件（GIF為每像素8位元）。

下表列出*`format`*和&#x200B;*`pixelType`*&#x200B;的有效組合、相應的HTTP響應MIME類型、是否可嵌入ICC配置檔案（請參見[iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)），以及可以應用的格式特定選項。

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> 格式</i> </b> </th> 
   <th class="entry"> <b> <i> pixelType</i> </b> </th> 
   <th class="entry"> <b> 回應MIME類型</b> </th> 
   <th class="entry"> <b>內嵌ICC設定檔</b> </th> 
   <th class="entry"> <b> 選項</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> jpeg, jpg, pjpeg </p> </td> 
   <td colname="col2"> <p>rgb，灰色， cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed=  </span>,  <span class="codeph"> pscan=  </span>, qlt=  <span class="codeph"> ,  </span> <span class="codeph"> xmpEmbed=  </span> </p> <p><span class="codeph"> pscan= </span>參數僅適用於pjpeg格式。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png, png,alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>png8、png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色， cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> 壓縮  </span> </span> <p> （<span class="codeph">無|lzw|zip|jpeg </span>） </p> <p>僅限tiff;「tiff-alpha」不支援jpeg壓縮。 </p> <p> <span class="codeph"> qlt=  </span> </p> <p> <span class="codeph"> 除非將 </span> 壓縮設為jpeg, <span class="varname"> 否 </span> 則會忽略 <span class="codeph"> qlt=  </span>。 </p> <p>, pathEmbed=, xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> swf,swf3,swf-alpha,swf-alpha3 </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>否 </p> <p> <p>注意： AdobeFlash Player忽略嵌入的ICC配置檔案。 </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt=  </span>，屬 <span class="codeph"> 性：:TrustedDomains  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> pdf </p> </td> 
   <td colname="col2"> <p>rgb，灰色， cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> 壓縮  </span> </span> <p> （<span class="codeph">無|zip|jpeg </span>）, <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> 除非將 </span> 壓縮設為jpeg, <span class="codeph"> <span class="varname"> 否 </span> </span> 則會忽略 <span class="codeph"> qlt=  </span>。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> eps </p> </td> 
   <td colname="col2"> <p>rgb，灰色， cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed=  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> gif, gif,alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> <p>轉換為灰色或rgb後，資料會轉換為浮動視窗。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>否 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> 量化=  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>webp, webp-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>否 </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> 壓 </span> </span> 縮( <span class="codeph"> 有損 </span>, <span class="codeph"> 無損 </span>) </p> <p> <span class="codeph"> qlt= </span> 對無損 <span class="codeph"> 忽 </span>略。 </p> <p>由於沒有使用WebP格式進行色度下採樣的概念，因此，如果使用帶有<span class="codeph"> qlt </span>的第二個值（例如<span class="codeph"> qlt=80,1 </span>），則忽略第二個值(<span class="codeph"> 1 </span>)。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000、jpeg2000-alpha </p> </td> 
   <td> <p>rgb，灰色 </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>否 </p> </td> 
   <td> <p>與上文相同。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpegxr,jpegxr-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>否 </p> </td> 
   <td> <p>與上文相同。 </p> </td> 
  </tr>
  <tr valign="top"> 
   <td> <p> 阿維夫 — 阿爾法航母 </p> </td> 
   <td> <p>rgb</p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>否 </p> </td> 
   <td> <p>與上文相同。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

要求屬性。 在`req=img`（預設值）或`req=mask`下，無論當前層設定如何均適用；否則將忽略。

*`type`* 若已指定，則 `iccProfile=` 會忽略。

## 預設 {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`，其中 *`defaultType`* 的處理方式如下：如果 `icc=` 已指定， *`defaultType`* 則與指定ICC配置檔案的像素類型相對應。如果未指定`icc=`，如果`req=mask`，則&#x200B;*`defaultType`*&#x200B;為`gray`，否則為`rgb`。

## 範例 {#section-b93222e652df404a84c69025247f07df}

**請求JPEG格式的低品質小型預覽影像（預設）:**

` http:// *`伺服器`*/myRootId/myImageId?qlt=60&wid=200`

**請求轉換為灰階的相同影像：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**以具有Alpha通道且高解析度的無損格式請求相同的影像：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**請求與灰度TIFF影像相同的影像的Alpha通道：**

` http:// *`伺服器`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**使用預設的ICC配置檔案將同一影像轉換為cmyk:**

` http:// *`伺服器`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**使用不同的ICC配置檔案將同一影像轉換為cmyk，並將該配置檔案嵌入TIFF影像中：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**以JPEG壓縮的TIF檔案形式傳送此影像，而不進行像素類型轉換：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**將影像轉換為雙色調GIF，具有鍵色透明度，並強制將顏色轉換為黑白：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**質量設定為80的有損：**

` http:// *`伺服器`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**Alpha無損：**

` http:// *`伺服器`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**質量設定為80的有損：**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**Alpha無損：**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**質量設定為80的有損：**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**Alpha無損：**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## 另請參閱 {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38),  [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76),  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517),  [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e),  [pathEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301),  [pscan](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135)。
