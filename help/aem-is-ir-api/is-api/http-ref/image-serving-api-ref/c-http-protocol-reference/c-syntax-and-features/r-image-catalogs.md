---
description: 本節將說明影像目錄的功能和語法。
solution: Experience Manager
title: 影像目錄
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c83ad2-a932-4df2-92ff-ab34d4a5b1a7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---

# 影像目錄{#image-catalogs}

本節將說明影像目錄的功能和語法。

影像目錄提供下列功能：

* 允許影像與某些中繼資料和修飾元命令持續關聯。

  影像目錄中的專案是使用捷徑記號`*`rootId/objId`*`來參照，其中`*`rootId`*`可識別影像目錄，而`*`objId`*`則可識別目錄中的資料記錄。
* 為特定請求屬性提供預設值，例如JPEG品質或是否要套用浮水印。
* 管理字型、ICC設定檔、巨集定義和請求範本

即使未定義特定的影像目錄，影像目錄的所有功能仍可透過預設目錄( [!DNL default.ini])使用。

如果請求URL路徑中的`*`rootId`*`符合特定影像目錄的`attribute::RootId`，則該目錄會成為此請求的主要目錄。 主目錄提供整個請求的預設屬性和設定。 如果找不到相符專案，則會改用預設目錄。

在`src=`或`mask=`命令中識別的目錄提供下列目錄屬性和資料給目前的圖層：

<table id="table_D3FA66EA5D054745900DE5A120885AA8"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>屬性/資料</b> </th> 
   <th class="entry"> <b>備註</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph">屬性：：DefaultExt</span> </p> </td> 
   <td> <p> 目前圖層中所有影像檔案路徑的預設副檔名 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">屬性：：Expiration</span> </p> </td> 
   <td> <p> <span class="codeph">目錄的預設：：Expiration</span>或目前圖層的到期（若未涉及目錄記錄） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">屬性：：Icc*</span> </p> </td> 
   <td> <p> 請求和/或目前圖層的工作ICC色彩設定檔、演算色彩比對方式和黑色點補償旗標 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">屬性：：RootPath</span> </p> </td> 
   <td> <p> 用於目前圖層的所有來源檔案路徑 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">屬性：：Resolution</span> </p> </td> 
   <td> <p> <span class="codeph">目錄的預設：：Resolution</span> （僅限） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">目錄：：錨點</span> </p> </td> 
   <td> <p> 目前圖層的<span class="codeph">錨點=</span>值的預設值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">目錄：：到期</span> </p> </td> 
   <td> <p> 所有圖層的最小到期值都會做為回覆影像的存留時間值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">目錄：：IccProfile</span> </p> </td> 
   <td> <p> 目前圖層的來源影像色彩設定檔 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">目錄：：Map</span> </p> </td> 
   <td> <p> 目前圖層的影像地圖資料 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">目錄：：MaskPath</span> </p> </td> 
   <td> <p> 目前圖層的<span class="codeph">遮罩預設=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">目錄：：Modifier</span> </p> </td> 
   <td> <p> 目前圖層的字首命令（如果為相同圖層指定，<span class="codeph">目錄：：Modifier</span>中的每個命令都可以由URL中的相同命令覆寫） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">目錄：：Path</span> </p> </td> 
   <td> <p> 目前圖層的來源影像檔案 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">目錄：：PostModifier</span> </p> </td> 
   <td> <p> 目前圖層的字尾命令（類似<span class="codeph"> catalog：：Modifier</span>，但<span class="codeph"> catalog：：PostModifier</span>中的命令會覆寫URL或<span class="codeph"> catalog：：Modifier</span>中指定的相同命令） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">目錄：：Resolution</span> </p> </td> 
   <td> <p> 目前圖層的物件解析度 </p> </td> 
  </tr> 
 </tbody> 
</table>

在相同圖層中，`src=`和`mask=`必須參考相同的影像目錄（如果有的話）。

在`icc=`命令中識別的目錄僅用於從目錄的ICC設定檔表格中查詢專案。 不涉及其他目錄屬性或資料。

如果`*`rootId`*`解析成目錄，且`*`objId`*`與此目錄中的`catalog::Id`相符，則`*`rootId/objId`*`會有效地由目錄專案取代，如下所示：

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## 另請參閱 {#section-00e4f6b39cd14244bcce537a3f831259}

[影像目錄參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)，[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)，[遮罩=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)，[錨點=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
