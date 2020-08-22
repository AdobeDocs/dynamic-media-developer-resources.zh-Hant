---
description: 回應影像格式。
seo-description: 回應影像格式。
seo-title: fmt
solution: Experience Manager
title: fmt
topic: Scene7 Image Serving - Image Rendering API
uuid: 29151740-3bbc-4c5e-bbc7-4afe9064ff5f
translation-type: tm+mt
source-git-commit: 515fcf8488eba7d9ca501a4182eaa73f1936488b
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 4%

---


# fmt{#fmt}

回應影像格式。

`fmt=format[,` `[`*`pixelType`*`]`,`[`*`compression`*`]]`

*`format`* — jpeg | jpg | pjpeg | png | png8 | png-alpha | png8-alpha | tif | tif-alpha | swf | swf-alpha | swf3 | swf3-alpha | eps | gif | gif-alpha | m3u8 | f4m |網頁 | webp-alpha | jpeg2000 | jpeg2000-alpha | jpegxr | jpegxr-alpha

| *`format`* | 說明 |
|---|---| 
| `jpeg` | 有損JPEG |
| `jpg` | 有損JPG |
| `pjpeg` | 漸進式 JPEG 圖像 |
| `png` | 24位元無損PNG |
| `png8` | 8位元無損PNG |
| `png-alpha` | 具有Alpha頻道的24位元無損PNG |
| `png8-alpha` | 具有Alpha頻道的8位無損PNG |
| `tif` | TIFF |
| `tif-alpha` | 含Alpha色版的TIFF |
| `pdf` | 內嵌於PDF的影像 |
| `eps` | 解壓縮的二進位封裝PostScript |
| `gif` | 2到256色的GIF |
| `gif-alpha` | 2到255色的GIF加上金鑰色透明度 |
| `swf` | 內嵌在Adobe AS2 swf檔案中的有損JPEG |
| `swf-alpha` | 有損JPEG和內嵌在Adobe AS2 swf檔案中的壓縮縮放遮色片 |
| `swf3` | 內嵌在Adobe AS3 swf檔案中的有損JPEG |
| `swf3-alpha` | 有損JPEG和內嵌在Adobe AS3 swf檔案中的壓縮縮放遮色片。 **注意**:swf和swf-alpha格式最適合用於ActionScript 2應用程式（Flash Player 8和更舊版本）。 建議將swf3和swf3-alpha用於ActionScript3應用程式（Flash Player 9和更新版本） |
| `m3u8` | Apple Streaming Server資訊清單格式 |
| `f4m` | Flash Streaming Server資訊清單格式 |
| `webp` | 有損和無損WebP |
| `webp-alpha` | 具有Alpha色版的有損和無損WebP |
| `jpeg2000` | 有損和無損JPEG 2000 |
| `jpeg2000-alpha` | 具有Alpha色版的有損與無損JPEG 2000 |
| `jpegxr` | 有損和無損JPEG XR |
| `jpegxr-alpha` | 具有Alpha色版的有損和無損JPEG XR |


| *`pixelType`* — rgb | 灰色 | cmy |
| *`pixelType`* | 說明 |
|---|---|
| `rgb` | 傳回RGB影像資料。 |
| `gray` | 傳回灰階影像資料。 |
| `cmyk` | 傳回CMYK影像資料。 |

| *`compression`* — none | lzw | 郵遞區號 | jpeg | 有損 | 無損 |
| *`compression`* | 說明 |
|---|---|
| `none` | 未壓縮 |
| `lzw` | LZW(Lempel-Ziv-Welch)壓縮（無損） |
| `zip` | &quot;Deflate&quot;壓縮（無損） |
| `jpeg` | JPEG壓縮（有損） |
| `lossy` | WebP、JPEG 2000和JPEG XR壓縮（有損） |
| `lossless` | WebP、JPEG 2000和JPEG XR壓縮（無損） |

* *`format`* 指定傳送至用戶端的影像資料的影像編碼格式，以及HTTP回應標題的對應回應MIME類型。
* *`pixelType`* 可用於在未指定時實現輸出色 `icc=` 域轉換。

   會套用對應的預設顏 *`pixelType`* 色描述檔。 如果停用色彩管理，則會套用天真的轉換。 *`pixelType`* 會在指定時 `icc=` 忽略，這會決定輸出像素類型。

* *`compression`* 僅當指定為 `tif`、、、、、 `tif-alpha`、或 `pdf`指定為A `webp``webp-alpha``jpeg2000``jpeg2000-alpha``jpegxr``jpegxr-alpha`*`format`*、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、B、 有關這些影像格式支援的壓縮選項，請參閱下表。

您可以使 `qlt=` 用以下格式設定JPEG編碼選項：JPEG、含JPEG壓縮的TIFF、含JPEG壓縮的PDF和SWF。 WebP、JPEG 2000和JPEG XR也會使用 `qlt=` ，但值會針對不同格式產生不同的品質。 若 `quantize=` 或 `fmt=gif` 使用 `fmt=gif-alpha`。 有關詳細資訊，請參閱命令說明。 其他格式沒有可設定的選項。

所有元件都會傳回8位元／像 *`formats`* 素元 *`pixelTypes`* 件，而GIF則會傳回8位元／像素元。

下表列出*`format`*和 *`pixelType`*、對應的HTTP回應MIME類型、ICC描述檔是否可內嵌(請參閱 [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e))，以及您可套用的格式特定選項的有效組合。

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
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span>, <span class="codeph"> pscan= </span>, qlt= <span class="codeph"> , </span><span class="codeph"> xmpEmbed= </span> </p> <p>pscan= <span class="codeph"> 參數 </span> 僅適用於pjpeg格式。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png, png-alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>png8, png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色， cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/tiff&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> 壓縮 </span> </span> <p> ( <span class="codeph"> 無|lzw|zip|jpeg </span>) </p> <p>僅「tiff」;'tiff-alpha'不支援jpeg壓縮。 </p> <p> <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> 若未將壓 </span> 縮設為jpeg，則 <span class="varname"> 會忽略 </span> qlt= <span class="codeph"> 值 </span>。 </p> <p>, pathEmbed=, xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> swf,swf3,swf-alpha,swf-alpha3 </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-shockwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>否 </p> <p> <p>注意： Adobe Flash Player會忽略內嵌的ICC設定檔。 </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>，屬 <span class="codeph"> 性：:TrustedDomains </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> pdf </p> </td> 
   <td colname="col2"> <p>rgb，灰色， cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> 壓縮 </span> </span> <p> ( <span class="codeph"> 無|zip|jpeg </span>), <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> 若未將壓 </span> 縮設為 <span class="codeph"> jpeg，則 <span class="varname"> 會忽略qlt= </span></span><span class="codeph"></span>。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> eps </p> </td> 
   <td colname="col2"> <p>rgb，灰色， cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/eps&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> gif, gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> <p>資料在轉換為灰色或RGB後會轉換為浮動視窗。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>否 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> 量化= </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>網路，webp-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/webp&gt; </span> </p> </td> 
   <td> <p>否 </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> 壓 </span> 縮 </span> ( <span class="codeph"> 有損 </span>、無 <span class="codeph"> 損 </span>) </p> <p> <span class="codeph"> 對於無損 </span> 資料，將忽略 <span class="codeph"> qlt= </span>。 </p> <p>由於WebP格式沒有色彩縮減取樣的概念，因此，如果您使用第二個值與 <span class="codeph"> qlt </span> (例如 <span class="codeph"> qlt=80,1 </span>)，則會忽略第二個值( <span class="codeph"> 1 </span>)。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000、jpeg2000-alpha </p> </td> 
   <td> <p>rgb，灰色 </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/jp2&gt; </span> </p> </td> 
   <td> <p>否 </p> </td> 
   <td> <p>與上文相同。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpegxr,jpegxr-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/vnd.ms-photo&gt; </span> </p> </td> 
   <td> <p>否 </p> </td> 
   <td> <p>與上文相同。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

請求屬性。 在（預設）或 `req=img``req=mask`;否則將忽略。

*`type`* 的值。 `iccProfile=`

## 預設 {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`，其中 *`defaultType`* 處理方式如下：如果 `icc=` 已指定， *`defaultType`* 則與指定ICC配置檔案的像素類型相對應。 如果 `icc=` 未指定， *`defaultType`* 則為 `gray` if，否則 `req=mask`為if `rgb`。

## 範例 {#section-b93222e652df404a84c69025247f07df}

**請求JPEG格式的小型、低品質預覽影像（預設）:**

` http:// *`伺服器`*/myRootId/myImageId?qlt=60&wid=200`

**請求轉換為灰階的相同影像：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**以無損格式，以Alpha色版和高解析度要求相同的影像：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**請求Alpha色版與灰階TIFF影像的相同影像：**

` http:// *`伺服器`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**使用預設的ICC描述檔，將相同的影像轉換為cmyk:**

` http:// *`伺服器`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**使用不同的ICC描述檔將相同的影像轉換為cmyk，並將描述檔內嵌在TIFF影像中：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**以TIF檔案的形式傳送此影像，並加上JPEG壓縮，而無需像素類型轉換：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**將影像轉換為雙色調GIF，具有關鍵色透明度，並強制色彩轉換為黑白：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**品質設定為80時有損：**

` http:// *`伺服器`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**使用Alpha進行無損：**

` http:// *`伺服器`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**品質設定為80時有損：**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**使用Alpha進行無損：**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**品質設定為80時有損：**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**使用Alpha進行無損：**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## 另請參閱 {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38), req=req= [, icc Embed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135), iccEmbed=嵌入路徑Embed=嵌入， pscanChomiz
