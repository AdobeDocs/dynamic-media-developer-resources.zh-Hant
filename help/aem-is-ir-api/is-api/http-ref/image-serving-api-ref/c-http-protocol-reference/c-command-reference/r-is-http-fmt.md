---
title: fmt
description: 回應影像格式。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67f8a58d-88f5-4993-9749-41a3c530adba
source-git-commit: b861d383d0a1af63ae18eb1e73231758c3352a55
workflow-type: tm+mt
source-wordcount: '1017'
ht-degree: 2%

---

# fmt{#fmt}

回應影像格式。

`fmt=format[,` `[`*`pixelType`*`]`，`[`*`compression`*`]]`

*`format`* - avif-alpha | avif | eps | f4m | gif-alpha | gif | heic | jpeg | jpeg2000-alpha | jpeg2000 | jpegxr-alpha | jpegxr | jpg | m3u8 | pdf | pjpeg | png-alpha | png | png8-alpha | png8 | swf-alpha | swf | swf3-alpha | swf3 | tif-alpha | tif | web-alpha | webp

| *`format`* | 說明 |
|---|---|
| `avif-alpha` | 含Alpha色版的AVIF有損和無損。 |
| `avif` | 有損且無損的AVIF。 |
| `eps` | 未壓縮的二進位封裝的PostScript。 |
| `f4m` | Flash串流伺服器資訊清單格式。 |
| `gif-alpha` | 2到255色GIF，加上關鍵色彩透明度。 |
| `gif` | 使用2到256色GIF。 |
| `heic` | 不失真HEIC。 如果不支援此格式，預設會從瀏覽器下載。 |
| `jpeg` | 有損JPEG。 |
| `jpeg2000-alpha` | 含Alpha色版的有損和無損JPEG2000。 |
| `jpeg2000` | 有損和無損JPEG2000。 |
| `jpegxr-alpha` | 含Alpha色版的有損和無損JPEGXR。 |
| `jpegxr` | 有損和無損JPEGXR。 |
| `jpg` | JPG有損。 |
| `m3u8` | Apple串流伺服器資訊清單格式。 |
| `pdf` | 內嵌於PDF中的影像。 |
| `pjpeg` | 漸進式JPEG。 |
| `png-alpha` | 含Alpha通道的24位元無失真PNG。 |
| `png` | 24位元無失真PNG。 |
| `png8-alpha` | 含Alpha色版的8位元無失真PNG。 |
| `png8` | 8位元無失真PNG。 |
| `swf-alpha` | AdobeAS2 SWF檔中內嵌的有損JPEG和Deflate-Compressed遮罩。 |
| `swf` | 內嵌於AdobeAS2 SWF檔中的有損JPEG。 |
| `swf3-alpha` | AdobeAS3 SWF檔中內嵌的有損JPEG和Deflate-Compressed遮罩。 **注意：** swf和swf-alpha格式最適合用於ActionScript2應用程式(Flash Player8或更早版本)。 建議將swf3和swf3-alpha格式用於ActionScript3應用程式(Flash Player9和更新版本)。 |
| `swf3` | 內嵌於AdobeAS3 SWF檔中的有損JPEG。 |
| `tif-alpha` | 使用Alpha色版TIFF。 |
| `tif` | TIFF。 |
| `webp-alpha` | 含Alpha色版的有損和無損WebP。 |
| `webp` | 有損和無損WebP。 |

| *`pixelType`* - rgb | 灰色 | cmyk |
| *`pixelType`* | 說明 |
|---|---|
| `cmyk` | 傳回CMYK影像資料。 |
| `gray` | 傳回灰階影像資料。 |
| `rgb` | 傳回RGB影像資料。 |

| *`compression`* - jpeg | 有損 | 不失真 | lzw | 無 | 郵遞區號 |
| *`compression`* | 說明 |
|---|---|
| `jpeg` | JPEG壓縮（失真）。 |
| `lossy` | JPEG2000、JPEGXR壓縮（失真）和WebP。 |
| `lossless` | HEIC、JPEG 2000和JPEGXR壓縮（不失真）和WebP。 |
| `lzw` | LZW (Lempel-Ziv-Welch)壓縮（不失真）。 |
| `none` | 未壓縮。 |
| `zip` | &quot;Deflate&quot;壓縮（不失真）。 |

* *`format`*&#x200B;會指定傳送至使用者端之影像資料的影像編碼格式，以及HTTP回應標頭的對應回應MIME型別。
* 未指定`icc=`時，可以使用&#x200B;*`pixelType`*&#x200B;進行輸出色域轉換。

  已套用對應至&#x200B;*`pixelType`*&#x200B;的預設色彩設定檔。 如果停用色彩管理，則會套用天真的轉換。 指定`icc=`時會忽略&#x200B;*`pixelType`*，這會決定輸出畫素型別。

* 只有在將`tif`、`tif-alpha`、`pdf`、`webp`、`webp-alpha`、`jpeg2000`、`jpeg2000-alpha`、`jpegxr`或`jpegxr-alpha`指定為&#x200B;*`format`*&#x200B;時，才允許&#x200B;*`compression`*。 如需這些影像格式支援的壓縮選項，請參閱下表。

您可以使用`qlt=`來設定下列格式的JPEG編碼選項：JPEG、使用JPEG壓縮的TIFF、使用JPEG壓縮的PDF以及SWF。 WebP、JPEG2000和JPEGXR也使用`qlt=`，但值會導致不同格式的不同品質。 如果`fmt=gif`或`fmt=gif-alpha`，請使用`quantize=`。 如需詳細資訊，請參閱命令說明。 其他格式沒有可設定的選項。

所有&#x200B;*`formats`*&#x200B;和&#x200B;*`pixelTypes`*&#x200B;會傳回8位元/畫素元件(GIF會傳回8位元/畫素)。

下表列出*`format`*與&#x200B;*`pixelType`*&#x200B;的有效組合、對應的HTTP回應MIME型別、是否可以內嵌ICC設定檔（請參閱[iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)），以及您可以套用哪些格式特定選項。

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>格式</i> </b> </th> 
   <th class="entry"> <b> <i> pixelType</i> </b> </th> 
   <th class="entry"> <b>回應MIME型別</b> </th> 
   <th class="entry"> <b>內嵌ICC設定檔</b> </th> 
   <th class="entry"> <b>選項</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> avif， avif-alpha </p> </td> 
   <td> <p>rgb</p> </td> 
   <td> <p> <span class="codeph"> &lt;image/avif&gt; </span> </p> </td> 
   <td> <p>否 </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname">壓縮</span> </span> （<span class="codeph">失真</span>，<span class="codeph">無失真</span>） </p> <p> 已忽略<span class="codeph"> qlt= </span> （因為<span class="codeph">不失真</span>）。 </p> <p>因為沒有WebP格式的色度縮減取樣概念，如果您使用含<span class="codeph"> qlt </span>的第二個值（例如，<span class="codeph"> qlt=80,1 </span>），則會忽略第二個值(<span class="codeph"> 1 </span>)。 </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> eps </p> </td> 
   <td colname="col2"> <p>rgb、灰色、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/eps&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> gif， gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> <p>資料在轉換為灰色或rgb之後，會轉換為調色盤。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>否 </p> </td> 
   <td colname="col5"> <p> <span class="codeph">量化= </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> heic </p> </td> 
   <td colname="col2"> <p>rgb </p> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/heic&gt; </span> </p> </td> 
   <td colname="col4"> <p>否 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000， jpeg2000-alpha </p> </td> 
   <td> <p>rgb，灰色 </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/jp2&gt; </span> </p> </td> 
   <td> <p>否 </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname">壓縮</span> </span> （<span class="codeph">失真</span>，<span class="codeph">無失真</span>） </p> <p> 已忽略<span class="codeph"> qlt= </span> （因為<span class="codeph">不失真</span>）。 </p> <p>因為沒有WebP格式的色度縮減取樣概念，如果您使用含<span class="codeph"> qlt </span>的第二個值（例如，<span class="codeph"> qlt=80,1 </span>），則會忽略第二個值(<span class="codeph"> 1 </span>)。 </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> jpeg， jpg， pjpeg </p> </td> 
   <td colname="col2"> <p>rgb、灰色、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span>，<span class="codeph"> pscan= </span>，<span class="codeph"> qlt= </span>，<span class="codeph"> xmpEmbed= </span> </p> <p><span class="codeph"> pscan= </span>引數僅適用於pjpeg格式。 </p> </td> 
  </tr>
  <tr valign="top"> 
   <td> <p>jpegxr， jpegxr-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/vnd.ms-photo&gt; </span> </p> </td> 
   <td> <p>否 </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname">壓縮</span> </span> （<span class="codeph">失真</span>，<span class="codeph">無失真</span>） </p> <p> 已忽略<span class="codeph"> qlt= </span> （因為<span class="codeph">不失真</span>）。 </p> <p>因為沒有WebP格式的色度縮減取樣概念，如果您使用含<span class="codeph"> qlt </span>的第二個值（例如，<span class="codeph"> qlt=80,1 </span>），則會忽略第二個值(<span class="codeph"> 1 </span>)。 </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> pdf </p> </td> 
   <td colname="col2"> <p>rgb、灰色、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname">壓縮</span> </span> <p> ( <span class="codeph"> none|zip|jpeg </span>)， <span class="codeph"> qlt= </span> </p> <p> 已忽略<span class="codeph"> qlt= </span>，除非<span class="codeph"> <span class="varname">壓縮</span> </span>設定為<span class="codeph"> jpeg </span>。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>png8， png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png， png-alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> swf，swf3， swf-alpha， swf-alpha3 </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-shockwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>否 </p> <p> <p>注意：AdobeFlash Player會忽略內嵌的ICC設定檔。 </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>，<span class="codeph">屬性：：TrustedDomains </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> tif， tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb、灰色、cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/tiff&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname">壓縮</span> </span> <p> (<span class="codeph"> none|lzw|zip|jpeg </span>) </p> <p>僅限'tiff'；'tiff-alpha'不支援jpeg壓縮。 </p> <p> <span class="codeph"> qlt= </span> </p> <p> 已忽略<span class="codeph"> qlt= </span>，除非<span class="varname">壓縮</span>設定為<span class="codeph"> jpeg </span>。 </p> <p>， pathEmbed=， xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>webp， webp-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/webp&gt; </span> </p> </td> 
   <td> <p>否 </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname">壓縮</span> </span> （<span class="codeph">失真</span>，<span class="codeph">無失真</span>） </p> <p> 已忽略<span class="codeph"> qlt= </span> （因為<span class="codeph">不失真</span>）。 </p> <p>因為沒有WebP格式的色度縮減取樣概念，如果您使用含<span class="codeph"> qlt </span>的第二個值（例如，<span class="codeph"> qlt=80,1 </span>），則會忽略第二個值(<span class="codeph"> 1 </span>)。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

要求屬性。 若為`req=img` （預設）或`req=mask`，則無論目前的圖層設定為何，皆適用；否則會忽略。

如果指定`iccProfile=`，則會忽略&#x200B;*`type`*。

## 預設 {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`，其中&#x200B;*`defaultType`*&#x200B;的處理方式如下：若指定`icc=`，*`defaultType`*&#x200B;會對應到指定ICC設定檔的畫素型別。 如果未指定`icc=`，則&#x200B;*`defaultType`*&#x200B;為`gray` （若為`req=mask`），否則為`rgb`。

## 範例 {#section-b93222e652df404a84c69025247f07df}

**要求小型、低品質的JPEG格式預覽影像（預設）：**

` http:// *`伺服器`*/myRootId/myImageId?qlt=60&wid=200`

**要求將相同的影像轉換為灰階：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**請以無損失格式要求相同影像（含Alpha色版和高解析度：**）

` http:// *`伺服器`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**要求與灰階TIFF影像相同影像的Alpha色版：**

` http:// *`伺服器`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**使用預設ICC設定檔將相同影像轉換為cmyk：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**使用其他ICC設定檔將相同影像轉換為cmyk，並將設定檔內嵌於TIFF影像中：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**以TIF檔形式傳遞此影像，並以JPEG壓縮方式傳遞，而不使用畫素型別轉換：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**將影像轉換為雙調GIF，具有關鍵色彩透明度，並強制色彩為黑白：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**品質設定為80的失真：**

` http:// *`伺服器`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**含Alpha的無損：**

` http:// *`伺服器`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**品質設定為80的失真：**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**含Alpha的無損：**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**品質設定為80的失真：**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**含Alpha的無損：**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## 另請參閱 {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ， [quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38)， [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)， [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)， [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)， [pathEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301)， [pscan](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135)。
