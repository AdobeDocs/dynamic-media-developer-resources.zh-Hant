---
description: 您可以使用影像伺服來管理目錄中的非影像內容，並透過個別的/is/content內容內容來提供。
seo-description: 您可以使用影像伺服來管理目錄中的非影像內容，並透過個別的/is/content內容內容來提供。
seo-title: 伺服靜態（非影像）內容
solution: Experience Manager
title: 伺服靜態（非影像）內容
topic: Scene7 Image Serving - Image Rendering API
uuid: bdb1383a-e02d-499f-be79-4a6dc501705c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 伺服靜態（非影像）內容{#serving-static-non-image-contents}

您可以使用影像伺服來管理目錄中的非影像內容，並透過個別的/is/content內容內容來提供。

此功能允許分別配置每個項目的TTL。

Image Serving支援以下命令： [!DNL /is/content]

<table id="simpletable_8A3AB1D1D20F4B6CBE86767E94735980"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" format="dita" scope="local"> 類型 </a> </p> </td> 
  <td class="stentry"> <p>內容類型篩選。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" format="dita" scope="local"> requin </a> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>、 <span class="codeph"> req=props </span>和req=exists <span class="codeph"></span> only. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" format="dita" scope="local"> 快取 </a> </p> </td> 
  <td class="stentry"> <p>允許禁用客戶端快取。 </p> </td> 
 </tr> 
</table>

## 基本語法 {#section-42103439011540b2b9da3b5eebb442cd}

<table id="simpletable_2F039A5BFA2C4E22B014F42ECBCDA0A2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 請 <span class="varname"> 求 </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="filepath"> http:// <span class="varname"> Server </span>/is/content[/catalog/ <span class="varname"> item </span>[? <span class="varname"> 修飾 </span>詞] </span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 伺服器 </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address </span>[ : <span class="varname"> 埠 </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 型 </span> 錄 </span> </p> </td> 
  <td class="stentry"> <p>目錄識別碼。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 項目 </span></span> </p> </td> 
  <td class="stentry"> <p>靜態內容項目ID。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 修飾 </span> 元 </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 命 </span>令*[&amp; <span class="varname"> 命令 </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 命令 </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span>= <span class="varname"> value </span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span></span> </p> </td> 
  <td class="stentry"> <p>支援的命令名之一。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 值 <span class="varname"></span></span> </p> </td> 
  <td class="stentry"> <p>命令值。 </p> </td> 
 </tr> 
</table>

## 靜態內容目錄 {#section-91014f17f0d543d7aaf24539b2d7d4b9}

靜態內容目錄類似於影像目錄，但支援的資料欄位較少：

<table id="table_71A565DF5EC94913AD35CB13B0C7A27D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>屬性／資料 </p> </th> 
   <th colname="col2" class="entry"> <p>附註 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 目錄：:Id </span> </p> </td> 
   <td colname="col2"> <p>此靜態內容項目的目錄記錄標識符。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 目錄：：路徑 </span> </p> </td> 
   <td colname="col2"> <p>此內容項的檔案路徑。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 目錄：：過期 </span> </p> </td> 
   <td colname="col2"> <p>此內容項目的TTL;屬 <span class="codeph"> 性：：未指 </span> 定或空白時使用過期。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 目錄：:TimeStamp </span> </p> </td> 
   <td colname="col2"> <p>檔案修改時間戳；在啟用屬性：:CacheValidationPolicy的目錄型驗證時 <span class="codeph"> 需要此選項 </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 目錄：:UserData </span> </p> </td> 
   <td colname="col2"> <p>與此靜態內容項目相關的可選元資料；可供具有req=userdata <span class="codeph"> 的客戶端使用 </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 目錄：:UserType </span> </p> </td> 
   <td colname="col2"> <p>可選資料類型；可用於使用type=命令篩選靜態內 <span class="codeph"> 容的請求 </span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 篩選靜態內容 {#section-4c41bf41ff994910840c1352683d1f37}

此機制可協助確保用戶端只收到符合其需求的內容。 假設靜態內容標籤了適當的 `catalog::UserType` 值，客戶端可以將命令 `type=` 添加到請求中。 「影像伺服」會將命令所提供的 `type=` 值與值進行比較，並 `catalog::UserType` 在發生不相符的情況下，傳回錯誤，而非可能不適當的內容。

## 視訊標題檔案 {#section-1ad25e10399e43eaa8ecb09b531dbf1a}

您可以封裝視訊標題檔案(WebVTT)、CSS或任何JSONP格式的文字檔案。 JSON回應說明如下。

* 對於WebVTT檔案，回應的MIME類型為text/javascript。 JSON不會傳回；而是傳回會呼叫具有JSON之方法的Javascript。 ID和處理常式都是選用的。
* 對於CSS檔案，回應的MIME類型為text/javascript。 ID和處理常式都是選用的。
* 依預設，會套用UTF-8編碼，以確保正確解碼。 預設大小限制為2 MB。

您也可以使用其他類型的計時中繼資料的追蹤。 每個追蹤元素的來源資料是由計時提示清單所組成的文字檔案。 提示可以包含JSON或CSV等格式的資料。

如需 [JSONP格式的詳細資訊](http://en.wikipedia.org/wiki/JSONP) ，請參閱http://en.wikipedia.org/wiki/JSONP。

如需 [JSON格式的詳細資訊](http://www.json.org) ，請參閱www.json.org。

## 另請參閱 {#section-7b28631016044a22a3a6762fd64771e9}

[type=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)，影像目錄 [參考](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5)
