---
description: 您可以使用「影像伺服」來管理目錄中的非影像內容，並透過個別的/is/content內容提供。
solution: Experience Manager
title: 為靜態（非影像）內容提供服務
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: adc3d972-b02d-40db-992e-acaa06b848ff
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# 為靜態（非影像）內容提供服務{#serving-static-non-image-contents}

您可以使用「影像伺服」來管理目錄中的非影像內容，並透過個別的/is/content內容提供。

此功能可讓您個別設定每個項目的TTL。

「影像伺服」在[!DNL /is/content]上支援以下命令：

<table id="simpletable_8A3AB1D1D20F4B6CBE86767E94735980"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" format="dita" scope="local"> 類型 </a> </p> </td> 
  <td class="stentry"> <p>內容類型篩選器。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" format="dita" scope="local"> 請求  </a> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata  </span>、  <span class="codeph"> req=props  </span>和req=exists  <span class="codeph">  </span> only. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" format="dita" scope="local"> 快取  </a> </p> </td> 
  <td class="stentry"> <p>允許禁用客戶端快取。 </p> </td> 
 </tr> 
</table>

## 基本語法 {#section-42103439011540b2b9da3b5eebb442cd}

<table id="simpletable_2F039A5BFA2C4E22B014F42ECBCDA0A2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 請求  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="filepath"> http://  <span class="varname"> server  </span>/is/content[/catalog/  <span class="varname"> item] </span>[?<span class="varname"> 修飾元 </span>]  </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 伺服器  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address  </span>[ : <span class="varname"> 埠 </span>]  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 目錄  </span> </span> </p> </td> 
  <td class="stentry"> <p>目錄識別碼。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 項目  </span> </span> </p> </td> 
  <td class="stentry"> <p>靜態內容項目ID。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 修飾符  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 命令 </span>*[&amp;  <span class="varname"> 命令 </span>]  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 命令  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName  </span>=  <span class="varname"> value  </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName  </span> </span> </p> </td> 
  <td class="stentry"> <p>支援的命令名之一。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>命令值。 </p> </td> 
 </tr> 
</table>

## 靜態內容目錄 {#section-91014f17f0d543d7aaf24539b2d7d4b9}

靜態內容目錄與影像目錄類似，但支援的資料欄位較少：

<table id="table_71A565DF5EC94913AD35CB13B0C7A27D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>屬性/資料 </p> </th> 
   <th colname="col2" class="entry"> <p>附註 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 目錄：:Id  </span> </p> </td> 
   <td colname="col2"> <p>此靜態內容項的目錄記錄標識符。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 目錄：：路徑  </span> </p> </td> 
   <td colname="col2"> <p>此內容項的檔案路徑。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 目錄：：過期  </span> </p> </td> 
   <td colname="col2"> <p>此內容項目的TTL;<span class="codeph">屬性：：如果未指定或為空，則使用過期</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 目錄：:TimeStamp  </span> </p> </td> 
   <td colname="col2"> <p>檔案修改時間戳；<span class="codeph">屬性：:CacheValidationPolicy </span>啟用基於目錄的驗證時需要。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 目錄：:UserData  </span> </p> </td> 
   <td colname="col2"> <p>與此靜態內容項目相關聯的可選元資料；可用於具有<span class="codeph"> req=userdata </span>的客戶端。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 目錄：:UserType  </span> </p> </td> 
   <td colname="col2"> <p>可選資料類型；可用<span class="codeph"> type=命令</span>來篩選靜態內容的請求。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 篩選靜態內容 {#section-4c41bf41ff994910840c1352683d1f37}

此機制可協助確保用戶端只接收符合其需求的內容。 假設靜態內容已加上適當的`catalog::UserType`值，用戶端可將`type=`命令新增至請求。 「影像伺服」將`type=`命令提供的值與`catalog::UserType`的值進行比較，並在出現不匹配時返回錯誤，而不是可能不適當的內容。

## 視頻標題檔案 {#section-1ad25e10399e43eaa8ecb09b531dbf1a}

您可以以JSONP格式封裝視訊標題檔案(WebVTT)、CSS或任何文字檔案。 JSON回應說明如下。

* 對於WebVTT檔案，回應的mime類型為text/javascript。 未傳回JSON;而是會傳回使用JSON呼叫方法的Javascript。 ID和處理常式均為選用。
* 對於CSS檔案，回應的mime類型為text/javascript。 ID和處理常式均為選用。
* 依預設，會套用UTF-8編碼，以確保正確解碼。 預設大小限制為2 MB。

您也可以對其他類型的計時中繼資料使用追蹤。 每個追蹤元素的來源資料是由計時提示清單所組成的文字檔案。 提示可包含JSON或CSV等格式的資料。

如需JSONP格式的詳細資訊，請參閱[http://en.wikipedia.org/wiki/JSONP](http://en.wikipedia.org/wiki/JSONP)。

如需JSON格式的詳細資訊，請參閱[www.json.org](http://www.json.org)。

## 另請參閱 {#section-7b28631016044a22a3a6762fd64771e9}

[type=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) ,  [req=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)，影 [像目錄參考](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5)
