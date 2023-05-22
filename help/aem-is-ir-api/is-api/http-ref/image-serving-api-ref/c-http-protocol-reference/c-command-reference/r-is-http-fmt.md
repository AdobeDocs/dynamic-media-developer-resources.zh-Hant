---
description: 響應影像格式。
solution: Experience Manager
title: fm
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67f8a58d-88f5-4993-9749-41a3c530adba
source-git-commit: 9d86f2acad638cbbcb80b48ead73443c76c895a9
workflow-type: tm+mt
source-wordcount: '877'
ht-degree: 4%

---

# fm{#fmt}

響應影像格式。

`fmt=format[,` `[`*`pixelType`*`]`,`[`*`compression`*`]]`

*`format`* - avifα | avif |eps |f4m | gif-alpha |gif |jpeg | jpeg2000-alpha | jpeg2000 | jpegxr-alpha |jpegxr | jpg | m3u8 |pdf | pjpeg | png-alpha | png | png8-alpha | png8 |swf-alpha |swf |swf3-alpha |swf3 | tif-alpha |tif | Web Alpha |web

| *`format`* | 說明 |
|---|---|
| `avif-alpha` | Alpha通道的有損和無損AVIF。 |
| `avif` | 有損和無損AVIF。 |
| `eps` | 未壓縮的二進位封裝PostScript。 |
| `f4m` | Flash流伺服器清單格式。 |
| `gif-alpha` | GIF具有2到255種顏色以及鍵色透明度。 |
| `gif` | GIF有2到256色。 |
| `jpeg` | 有損JPEG。 |
| `jpeg2000-alpha` | 有損和無損JPEG2000與Alpha通道。 |
| `jpeg2000` | 有損和無損JPEG2000。 |
| `jpegxr-alpha` | 具有Alpha通道的有損和無損JPEGXR。 |
| `jpegxr` | 有損和無損JPEGXR。 |
| `jpg` | 有損JPG。 |
| `m3u8` | Apple流伺服器清單格式。 |
| `pdf` | 嵌入在PDF中的影像。 |
| `pjpeg` | 進步JPEG。 |
| `png-alpha` | 24位無損PNG（帶Alpha通道）。 |
| `png` | 24位無損PNG。 |
| `png8-alpha` | 帶Alpha通道的8位無損PNG。 |
| `png8` | 8位無損PNG。 |
| `swf-alpha` | 有損JPEG和嵌入到AdobeAS2 swf檔案中的壓縮蒙版。 |
| `swf` | 有損JPEG嵌入到AdobeAS2 swf檔案中。 |
| `swf3-alpha` | 有損JPEG和嵌入到AdobeAS3swf檔案中的壓縮蒙版。 **注：** swf和swf-alpha格式最適合ActionScript2應用程式(Flash Player8和更早版本)。 建議將swf3和swf3-alpha格式用於ActionScript3應用程式(Flash Player9及更高版本)。 |
| `swf3` | 嵌入到JPEGAS3swf檔案中的有損Adobe。 |
| `tif-alpha` | TIFF帶α通道。 |
| `tif` | TIFF。 |
| `webp-alpha` | 具有Alpha通道的有損和無損WebP。 |
| `webp` | 有損和無損WebP。 |

| *`pixelType`* – rgb | 灰 | 色 |
| *`pixelType`* | 說明 |
|---|---|
| `cmyk` | 返回CMYK影像資料。 |
| `gray` | 返回灰階影像資料。 |
| `rgb` | 返回RGB影像資料。 |

| *`compression`* – none | 洛茲 | 郵遞區號 | jpeg | 損耗 | 無損 |
| *`compression`* | 說明 |
|---|---|
| `jpeg` | JPEG壓縮（有損）。 |
| `lossy` | WebP、JPEG2000和JPEGXR壓縮（有損）。 |
| `lossless` | WebP、JPEG2000和JPEGXR壓縮（無損）。 |
| `lzw` | LZW(Lempel-Ziv-Welch)壓縮（無損）。 |
| `none` | 未壓縮。 |
| `zip` | &quot;Deflate&quot;壓縮（無損）。 |

* *`format`* 指定發送到客戶端的影像資料的影像編碼格式和HTTP響應標頭的相應響應MIME類型。
* *`pixelType`* 可用於在 `icc=` 未指定。

   與 *`pixelType`* 的子菜單。 如果禁用顏色管理，則應用天真的轉換。 *`pixelType`* 忽略 `icc=` 指定，它確定輸出像素類型。

* *`compression`* 僅當 `tif`。 `tif-alpha`。 `pdf`。 `webp`。 `webp-alpha`。 `jpeg2000`。 `jpeg2000-alpha`。 `jpegxr`或 `jpegxr-alpha` 指定為 *`format`*。 有關這些影像格式支援的壓縮選項，請參閱下表。

您可以使用 `qlt=` 要設定這些格式的JPEG編碼選項：JPEG、TIFF與JPEG壓縮、PDF與JPEG壓縮和SWF。 WebP、JPEG2000和JPEGXR也使用 `qlt=` 但是，這些值會導致不同格式的不同品質。 使用 `quantize=` 如果 `fmt=gif` 或 `fmt=gif-alpha`。 有關詳細資訊，請參閱命令說明。 其他格式沒有可設定的選項。

每像素8位的元件返回 *`formats`* 和 *`pixelTypes`* (每像素8位用於GIF)。

下表列出了*的有效組合`format`*和 *`pixelType`*，相應的HTTP響應MIME類型，是否可以嵌入ICC配置檔案(請參見 [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e))，以及您可以應用的格式特定選項。

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> 格式</i> </b> </th> 
   <th class="entry"> <b> <i> 像素類型</i> </b> </th> 
   <th class="entry"> <b> 響應MIME類型</b> </th> 
   <th class="entry"> <b>嵌入ICC配置檔案</b> </th> 
   <th class="entry"> <b> 選項</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> jpeg, jpg, pjpeg </p> </td> 
   <td colname="col2"> <p>rgb，灰色，cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span>。 <span class="codeph"> pscan= </span>。 <span class="codeph"> qlt= </span>。 <span class="codeph"> xmpEmbed= </span> </p> <p>的 <span class="codeph"> pscan= </span> 參數僅適用於pjpeg格式。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png, png,alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>png8、png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> tif,tif-α </p> </td> 
   <td colname="col2"> <p>rgb，灰色，cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/tiff&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> 壓縮 </span> </span> <p> ( <span class="codeph"> 無|lzw|zip|jpeg </span>) </p> <p>僅「tiff」；「tiff-alpha」不支援jpeg壓縮。 </p> <p> <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> 除非 <span class="varname"> 壓縮 </span> 設定為 <span class="codeph"> jpeg </span>。 </p> <p>,pathEmbed=,xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> swf,swf3,swf-alpha,swf-alpha3 </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-shockwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>否 </p> <p> <p>注：AdobeFlash Player忽略嵌入的ICC配置檔案。 </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>。 <span class="codeph"> 屬性：:TrustedDomains </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> pdf </p> </td> 
   <td colname="col2"> <p>rgb，灰色，cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> 壓縮 </span> </span> <p> ( <span class="codeph"> 無|zip|jpeg </span>) <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> 除非 <span class="codeph"> <span class="varname"> 壓縮 </span> </span> 設定為 <span class="codeph"> jpeg </span>。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> 蜂 </p> </td> 
   <td colname="col2"> <p>rgb，灰色，cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/eps&gt; </span> </p> </td> 
   <td colname="col4"> <p>是 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> gif, gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb，灰色 </p> <p>資料在轉換為灰色或rgb後轉換為調色板。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>否 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> 量化= </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>Webp,Webpα </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/webp&gt; </span> </p> </td> 
   <td> <p>否 </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> 壓縮 </span> </span> ( <span class="codeph"> 損耗 </span>。 <span class="codeph"> 無損 </span>) </p> <p> <span class="codeph"> qlt= </span> 忽略 <span class="codeph"> 無損 </span>。 </p> <p>因為沒有WebP格式的色度下採樣的概念，所以如果您使用第二個值 <span class="codeph"> QLT </span> (例如， <span class="codeph"> qlt=80,1 </span>)第二個值( <span class="codeph"> 1 </span>)。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000、jpeg2000-alpha </p> </td> 
   <td> <p>rgb，灰色 </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/jp2&gt; </span> </p> </td> 
   <td> <p>否 </p> </td> 
   <td> <p>和上面一樣。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpegxr-jpegxr-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/vnd.ms-photo&gt; </span> </p> </td> 
   <td> <p>否 </p> </td> 
   <td> <p>和上面一樣。 </p> </td> 
  </tr>
  <tr valign="top"> 
   <td> <p> 阿維夫 </p> </td> 
   <td> <p>rgb</p> </td> 
   <td> <p> <span class="codeph"> &lt;image/avif&gt; </span> </p> </td> 
   <td> <p>否 </p> </td> 
   <td> <p>和上面一樣。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

請求屬性。 應用，而不考慮當前圖層設定 `req=img` （預設）或 `req=mask`;否則忽略。

*`type`* 如果忽略 `iccProfile=` 。

## 預設 {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`的子菜單。 *`defaultType`* 如下所示：如果 `icc=` 已指定， *`defaultType`* 與指定ICC配置檔案的像素類型相對應。 如果 `icc=` 未指定， *`defaultType`* 是 `gray` 如果 `req=mask`，否則 `rgb`。

## 範例 {#section-b93222e652df404a84c69025247f07df}

**以JPEG格式請求低質量的小預覽影像（預設）:**

` http:// *`伺服器`*/myRootId/myImageId?qlt=60&wid=200`

**請求將同一影像轉換為灰度：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**以Alpha通道和高解析度的無損格式請求相同的影像：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**請求Alpha通道以獲取與灰度TIFF影像相同的影像：**

` http:// *`伺服器`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**使用預設ICC配置檔案將同一影像轉換為cmyk:**

` http:// *`伺服器`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**使用不同的ICC配置檔案將同一影像轉換為cmyk，並將該配置檔案嵌入TIFF影像：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**將此影像作為TIF檔案進行傳輸，該檔案具有JPEG壓縮，而無像素類型轉換：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**將影像轉換為具有鍵色透明度的雙調GIF，並將強制顏色轉換為黑白：**

` http:// *`伺服器`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**質量設定為80有損：**

` http:// *`伺服器`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**Alpha無損：**

` http:// *`伺服器`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**質量設定為80有損：**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**Alpha無損：**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**質量設定為80有損：**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**Alpha無損：**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## 另請參閱 {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) 。 [量化=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38)。 [請求=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)。 [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)。 [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)。 [pathEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301)。 [掃描](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135)。
