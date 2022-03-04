---
description: 本節介紹了影像目錄的功能和語法。
solution: Experience Manager
title: 影像目錄
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c83ad2-a932-4df2-92ff-ab34d4a5b1a7
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 0%

---

# 影像目錄{#image-catalogs}

本節介紹了影像目錄的功能和語法。

映像目錄提供以下功能：

* 允許將影像與某些元資料和修飾符命令持久關聯。

   使用快捷方式表示法引用影像目錄中的條目 `*`rootId/objId`*`，也請參見Wiki頁。 `*`根ID`*` 標識影像目錄， `*`objId`*` 標識目錄中的資料記錄。
* 為某些請求屬性(如JPEG質量或是否應用水印)提供預設值。
* 管理字型、ICC配置檔案、宏定義和請求模板

即使沒有定義特定的映像目錄，也可以通過預設目錄( [!DNL default.ini])。

如果 `*`根ID`*` 請求的URL路徑匹配 `attribute::RootId` 指定的映像目錄中，該目錄將成為此請求的主目錄。 主目錄提供整個請求的預設屬性和設定。 如果找不到匹配項，則改用預設目錄。

在 `src=` 或 `mask=` 命令將以下目錄屬性和資料提供給當前層：

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
   <td> <p> <span class="codeph"> 屬性：：到期</span> </p> </td> 
   <td> <p> 預設 <span class="codeph"> 目錄：：到期</span> 或當前層的到期（如果未涉及目錄記錄） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：:Icc*</span> </p> </td> 
   <td> <p> 請求和/或當前層的工作ICC顏色配置檔案、渲染意圖和黑點補償標誌 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：:RootPath</span> </p> </td> 
   <td> <p> 用於當前層的所有源檔案路徑 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：：解析度</span> </p> </td> 
   <td> <p> 預設 <span class="codeph"> 目錄：：解析</span> 僅 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：：錨點</span> </p> </td> 
   <td> <p> 預設 <span class="codeph"> 錨=</span> 當前圖層的值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：：到期</span> </p> </td> 
   <td> <p> 所有層的最小到期值被用作回復影像的生存時間值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：:IccProfile</span> </p> </td> 
   <td> <p> 當前圖層的源影像顏色配置檔案 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：：映射</span> </p> </td> 
   <td> <p> 當前層的影像映射資料 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：:MaskPath</span> </p> </td> 
   <td> <p> 預設 <span class="codeph"> 掩碼=</span> 當前層 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：：修改量</span> </p> </td> 
   <td> <p> 當前層的前置詞命令( <span class="codeph"> 目錄：：修改量</span> 可以由URL中的同一命令覆蓋（如果為同一層指定） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：：路徑</span> </p> </td> 
   <td> <p> 當前圖層的源影像檔案 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：:PostModifier</span> </p> </td> 
   <td> <p> 當前層的postfix命令(類似於 <span class="codeph"> 目錄：：修改量</span>，但是 <span class="codeph"> 目錄：:PostModifier</span> 覆蓋在URL或 <span class="codeph"> 目錄：：修改量</span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目錄：：解析</span> </p> </td> 
   <td> <p> 當前圖層的對象解析度 </p> </td> 
  </tr> 
 </tbody> 
</table>

在同一層內， `src=` 和 `mask=` 必須引用同一映像目錄（如果有）。

在 `icc=` 命令僅用於從目錄的ICC配置檔案表查找條目。 不涉及其他目錄屬性或資料。

如果， `*`根ID`*` 解析為目錄， `*`objId`*` 與 `catalog::Id` 在這個目錄中，然後 `*`rootId/objId`*` 實際上被目錄條目替換為類似的：

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## 另請參閱 {#section-00e4f6b39cd14244bcce537a3f831259}

[影像目錄引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)。 [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)。 [掩碼=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)。 [錨=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
