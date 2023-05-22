---
title: 服務靜態（非影像）內容
description: 可以使用影像服務管理目錄中的非影像內容，並通過單獨的/is/content上下文來服務。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: adc3d972-b02d-40db-992e-acaa06b848ff
source-git-commit: d1df6e943747f9db12c08003647aee840fdfcc0a
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 0%

---

# 服務靜態（非影像）內容{#serving-static-non-image-contents}

可以使用影像服務管理目錄中的非影像內容，並通過單獨的/is/content上下文來服務。

此功能允許單獨配置每個項的TTL。

映像服務支援以下命令： [!DNL /is/content]:

<table id="simpletable_8A3AB1D1D20F4B6CBE86767E94735980"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" format="dita" scope="local"> 類型 </a> </p> </td> 
  <td class="stentry"> <p>內容類型篩選器。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" format="dita" scope="local"> 請求 </a> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>。 <span class="codeph"> req=props </span>, <span class="codeph"> req=exiss </span> 只是。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" format="dita" scope="local"> 快取 </a> </p> </td> 
  <td class="stentry"> <p>允許禁用客戶端快取。 </p> </td> 
 </tr> 
</table>

## 基本語法 {#section-42103439011540b2b9da3b5eebb442cd}

<table id="simpletable_2F039A5BFA2C4E22B014F42ECBCDA0A2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 請求 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="filepath"> http:// <span class="varname"> 伺服器 </span>/is/content[/catalog//////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////// <span class="varname"> 物料 </span>][? <span class="varname"> 修飾 </span>] </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 伺服器 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 伺服器地址 </span>[ : <span class="varname"> 埠 </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 目錄 </span> </span> </p> </td> 
  <td class="stentry"> <p>目錄標識符。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 物料 </span> </span> </p> </td> 
  <td class="stentry"> <p>靜態內容項ID。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 修飾 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 命令 </span>*[&amp; <span class="varname"> 命令 </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 命令 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmd名稱 </span>= <span class="varname"> 值 </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmd名稱 </span> </span> </p> </td> 
  <td class="stentry"> <p>支援的命令名稱之一。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 值 </span> </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> 目錄：:ID </span> </p> </td> 
   <td colname="col2"> <p>此靜態內容項的目錄記錄標識符。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 目錄：：路徑 </span> </p> </td> 
   <td colname="col2"> <p>此內容項的檔案路徑。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 目錄：：到期 </span> </p> </td> 
   <td colname="col2"> <p>此內容項的TTL; <span class="codeph"> 屬性：：到期 </span> 如果未指定或為空，則使用。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 目錄：:TimeStamp </span> </p> </td> 
   <td colname="col2"> <p>檔案修改時間戳；啟用基於目錄的驗證時需要 <span class="codeph"> 屬性：:CacheValidationPolicy </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 目錄：:UserData </span> </p> </td> 
   <td colname="col2"> <p>與此靜態內容項關聯的可選元資料；可供客戶端使用 <span class="codeph"> req=userdata </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 目錄：:UserType </span> </p> </td> 
   <td colname="col2"> <p>可選資料類型；可用於篩選靜態內容的請求 <span class="codeph"> type=命令 </span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 篩選靜態內容 {#section-4c41bf41ff994910840c1352683d1f37}

此機制可幫助確保客戶端只接收適合其需要的內容。 假設靜態內容標籤了適當的 `catalog::UserType` 值，客戶端可以 `type=` 命令。 影像服務比較與 `type=` 的值 `catalog::UserType` 並且，如果存在不匹配，則返回錯誤而不是可能不適當的內容。

## 視頻標題檔案 {#section-1ad25e10399e43eaa8ecb09b531dbf1a}

可以封裝視頻標題檔案(WebVTT)、CSS或任何JSONP格式的文本檔案。 JSON響應說明如下。

* 對於WebVTT檔案，響應的mime類型為text/javascript。 未返回JSON;而是返回調用JSON方法的JavaScript。 ID和處理程式都是可選的。
* 對於CSS檔案，響應的mime類型為text/javascript。 ID和處理程式都是可選的。
* 預設情況下，應用UTF-8編碼以確保正確解碼。 預設大小限制為2 MB。

您還可以對其他類型的定時元資料使用跟蹤。 每個軌道元素的源資料是由定時提示清單組成的文本檔案。 提示可以包括JSON或CSV格式的資料。

請參閱 [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) 的子菜單。

請參閱 [www.json.org](https://www.json.org/json-en.html) 的子菜單。

## 另請參閱 {#section-7b28631016044a22a3a6762fd64771e9}

[類型=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) 。 [請求=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)。 [影像目錄引用](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5)
