---
description: 回應影像格式。
solution: Experience Manager
title: fmt
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 3%

---


# fmt&lt;a0/{#fmt}

回應影像格式。

`fmt=format [,pixelType ]`

<table id="simpletable_66FAABB7BD7A4BBB815A570BEA4C1AE8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 格式</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> jpeg | png | png-alpha | tif | tif-alpha | swf | pdf | gif | gif-alpha | fxg | fxgraw</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> 指定傳送至用戶端的影像資料的影像編碼格式，以及HTTP回覆標題的對應回應MIME類型。 </p> <p> <span class="codeph">  jpeg </span>:有損JPEG </p> <p> <span class="codeph"> png  </span>:無損PNG </p> <p> <span class="codeph"> png-alpha </span>:具有alpha色版的無損PNG </p> <p> <span class="codeph">  tif  </span>:TIFF </p> <p> <span class="codeph"> tif-alpha  </span>:含Alpha色版的TIFF </p> <p> <span class="codeph">  swf  </span>:有損JPEG嵌入Adobeswf檔案 </p> <p> <span class="codeph"> pdf  </span>:內嵌在PDF中的影像 </p> <p> <span class="codeph"> gif  </span>:2到256色的GIF </p> <p> <span class="codeph"> gif-alpha  </span>:2到255色的GIF加上金鑰色透明度 </p> <p> <span class="codeph"> fxg  </span>:FXG含變數並套用DOM控制 </p> <p> <span class="codeph">  fxgraw  </span>:原始FXG儲存在伺服器上 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pixelType</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> rgb |灰色 | cmyk</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> 可用來影響輸出色域。 </p> <p> <span class="codeph">  rgb  </span>:傳回RGB影像資料 </p> <p> <span class="codeph"> 灰色 </span>:傳回灰階影像資料 </p> <p> <span class="codeph"> cmyk  </span>:傳回CMYK影像資料 </p> </td> 
 </tr> 
</table>

`tiffCompression` 的值，則僅當tif,tif-alpha指定為格式時才允許。有關這些影像格式支援的壓縮選項，請參閱下表。

`qlt=` 可用來設定下列格式的JPEG編碼選項：JPEG、含JPEG壓縮的TIFF。如果fmt=gif或fmt=gif-alpha，則可使用quantize=。 有關詳細資訊，請參閱命令說明。 其他格式沒有可設定的選項。

針對所有格式和`pixelTypes[7]`傳回每像素8位元元件。

下表列出格式的有效組合和`pixelType`，即對應的HTTP響應MIME類型。

<table id="table_54AFE58185004C74971EFBA845E177B6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p><span class="varname"> 格式</span> </p> </th> 
   <th colname="col2" class="entry"> <p><span class="varname"> pixelType</span> </p> </th> 
   <th colname="col3" class="entry"> <p>回應MIME類型 </p> </th> 
   <th colname="col4" class="entry"> <p>內嵌ICC設定檔 </p> </th> 
   <th colname="col5" class="entry"> <p>選項 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>jpeg </p> </td> 
   <td> <p>rgb，灰色， cmyk </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p><span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>png, png-alpha </p> </td> 
   <td> <p>rgb，灰色 </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>tif, tif-alpha </p> </td> 
   <td> <p>rgb，灰色， cmyk </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p><span class="codeph"> <span class="varname"> tiffCompression</span> (none | lzw | zip | jpeg), qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>swf,swf-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p>&lt;application&gt; </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p><span class="codeph"> qlt=  </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>pdf </p> </td> 
   <td> <p>rgb，灰色， cmyk </p> </td> 
   <td> <p>&lt;application&gt; </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>gif, gif-alpha </p> </td> 
   <td> <p>rgb，灰色 </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>無 </p> </td> 
   <td> <p><span class="codeph"> 量化=</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-2135175ab3ec453f9f5388d5690b0da4}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=swf]
