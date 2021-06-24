---
description: 本節將說明影像目錄的功能和語法。
solution: Experience Manager
title: 影像目錄
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 54c83ad2-a932-4df2-92ff-ab34d4a5b1a7
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 0%

---

# 影像目錄{#image-catalogs}

本節將說明影像目錄的功能和語法。

影像目錄提供下列功能：

* 允許將影像與某些元資料和修飾符命令持久關聯。

   影像目錄中的條目使用快捷記號`*`rootId/objId`*`引用，其中`*`rootId`*`標識影像目錄，`*`objId`*`標識目錄中的資料記錄。
* 為某些請求屬性（如JPEG質量或是否要應用水印）提供預設值。
* 管理字型、ICC配置檔案、宏定義和請求模板

即使未定義特定的影像目錄，影像目錄的所有功能也可通過預設目錄([!DNL default.ini])提供。

如果請求的URL路徑中的`*`rootId`*`符合特定影像目錄的`attribute::RootId`，該目錄將成為此請求的主要目錄。 主目錄提供整個請求的預設屬性和設定。 如果找不到相符項目，則會改用預設目錄。

`src=`或`mask=`命令中標識的目錄向當前層提供以下目錄屬性和資料：

<table id="table_D3FA66EA5D054745900DE5A120885AA8"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 屬性/資料</b> </th> 
   <th class="entry"> <b> 附註</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：:DefaultExt</span> </p> </td> 
   <td> <p> 當前圖層中所有影像檔案路徑的預設副檔名 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：：過期</span> </p> </td> 
   <td> <p> <span class="codeph">目錄的預設值：：過期</span>；如果未涉及目錄記錄，則當前層過期 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：:Icc*</span> </p> </td> 
   <td> <p> 請求和/或當前圖層的工作ICC顏色配置檔案、渲染目的和黑點補償標誌 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：:RootPath</span> </p> </td> 
   <td> <p> 用於當前層的所有源檔案路徑 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：：解析度</span> </p> </td> 
   <td> <p> <span class="codeph">目錄：:Resolution</span>的預設值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：：錨點</span> </p> </td> 
   <td> <p> 預設值為當前層的<span class="codeph">錨點=</span>值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：：過期</span> </p> </td> 
   <td> <p> 所有圖層的最小過期值都用作回復影像的存留時間值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：:IccProfile</span> </p> </td> 
   <td> <p> 當前圖層的源影像顏色配置檔案 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：:Map</span> </p> </td> 
   <td> <p> 當前層的影像映射資料 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：:MaskPath</span> </p> </td> 
   <td> <p> 當前層<span class="codeph">掩碼=</span>的預設值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：：修飾詞</span> </p> </td> 
   <td> <p> 當前層的前置詞命令（<span class="codeph">目錄：:Modifier</span>中的每個命令可由URL中的同一命令覆蓋，如果為同一層指定） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：：路徑</span> </p> </td> 
   <td> <p> 當前圖層的源影像檔案 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：:PostModifier</span> </p> </td> 
   <td> <p> 當前層的postfix命令（類似於<span class="codeph">目錄：:Modifier</span>，但<span class="codeph">目錄：:PostModifier</span>中的命令會覆蓋URL或<span class="codeph">目錄：:Modifier</span>中指定的相同命令） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：：解析度</span> </p> </td> 
   <td> <p> 當前層的對象解析度 </p> </td> 
  </tr> 
 </tbody> 
</table>

在相同層內，`src=`和`mask=`必須參考相同的影像目錄（如果有）。

`icc=`命令中標識的目錄僅用於從目錄的ICC配置檔案表查找條目。 不涉及其他目錄屬性或資料。

如果`*`rootId`*`解析為目錄，且`*`objId`*`與此目錄中的`catalog::Id`相符，則`*`rootId/objId`*`會以類似以下的目錄項目有效取代：

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## 另請參閱 {#section-00e4f6b39cd14244bcce537a3f831259}

[影像目錄參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3),  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
