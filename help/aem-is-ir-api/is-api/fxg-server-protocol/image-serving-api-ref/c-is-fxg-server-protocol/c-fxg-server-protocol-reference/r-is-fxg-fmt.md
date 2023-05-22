---
description: 響應影像格式。
solution: Experience Manager
title: fm
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e179fc51-0461-4000-99eb-4390c35d5606
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 3%

---

# fm{#fmt}

響應影像格式。

`fmt=format [,pixelType ]`

<table id="simpletable_66FAABB7BD7A4BBB815A570BEA4C1AE8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 格式</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> jpeg | png | png-alpha |tif | tif-alpha |swf |pdf |gif | gif-alpha | fxg | fxgraw</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> 指定發送到客戶端的影像資料的影像編碼格式和HTTP答復標頭的相應響應MIME類型。 </p> <p> <span class="codeph">  jpeg </span>:有損JPEG </p> <p> <span class="codeph"> png </span>:無損PNG </p> <p> <span class="codeph"> pngα </span>:具有α通道的無損PNG </p> <p> <span class="codeph">  提 </span>:TIFF </p> <p> <span class="codeph"> 提夫α </span>:具有α通道的TIFF </p> <p> <span class="codeph">  swer </span>:有損JPEG嵌入到Adobeswf檔案中 </p> <p> <span class="codeph"> pdf </span>:嵌入在PDF中的影像 </p> <p> <span class="codeph"> gif </span>:GIF,2到256色 </p> <p> <span class="codeph"> gif-α </span>:GIF,2到255色，加上鍵色透明 </p> <p> <span class="codeph"> fxg </span>:帶變數的FXG和應用DOM操作 </p> <p> <span class="codeph">  fxgraw </span>:原始FXG儲存在伺服器上 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 像素類型</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 三 |灰色 |cmyk</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> 可用於影響輸出顏色空間。 </p> <p> <span class="codeph">  三 </span>:返回RGB影像資料 </p> <p> <span class="codeph"> 灰 </span>:返回灰階影像資料 </p> <p> <span class="codeph"> 色 </span>:返回CMYK影像資料 </p> </td> 
 </tr> 
</table>

`tiffCompression` 的子菜單。 有關這些影像格式支援的壓縮選項，請參閱下表。

`qlt=` 可用於為以下格式設定JPEG編碼選項：JPEG,TIFF和JPEG壓縮。 如果fmt=gif或fmt=gif-alpha，則可以使用quantize=。 有關詳細資訊，請參閱命令說明。 其他格式沒有可設定的選項。

對於所有格式和 `pixelTypes[7]`。

下表列出了格式和 `pixelType`，相應的HTTP響應MIME類型。

<table id="table_54AFE58185004C74971EFBA845E177B6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p><span class="varname"> 格式</span> </p> </th> 
   <th colname="col2" class="entry"> <p><span class="varname"> 像素類型</span> </p> </th> 
   <th colname="col3" class="entry"> <p>響應MIME類型 </p> </th> 
   <th colname="col4" class="entry"> <p>嵌入ICC配置檔案 </p> </th> 
   <th colname="col5" class="entry"> <p>選項 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>jpeg </p> </td> 
   <td> <p>rgb，灰色，cmyk </p> </td> 
   <td> <p>&lt;image/jpeg&gt; </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p><span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>png, png,alpha </p> </td> 
   <td> <p>rgb，灰色 </p> </td> 
   <td> <p>&lt;image/png&gt; </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>tif,tif-α </p> </td> 
   <td> <p>rgb，灰色，cmyk </p> </td> 
   <td> <p>&lt;image/tiff&gt; </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p><span class="codeph"> <span class="varname"> tiff壓縮</span> （無） | lzw |zip | jpeg), qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>swf,swf,alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p>&lt;application/x-shockwave-flash&gt; </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p><span class="codeph"> qlt= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>pdf </p> </td> 
   <td> <p>rgb，灰色，cmyk </p> </td> 
   <td> <p>&lt;application/pdf&gt; </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>gif, gif-alpha </p> </td> 
   <td> <p>rgb，灰色 </p> </td> 
   <td> <p>&lt;image/gif&gt; </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p><span class="codeph"> 量化=</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-2135175ab3ec453f9f5388d5690b0da4}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=swf]
