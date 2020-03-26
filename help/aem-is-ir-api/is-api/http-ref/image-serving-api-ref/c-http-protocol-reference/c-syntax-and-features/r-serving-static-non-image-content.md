---
description: 'null'
seo-description: 'null'
seo-title: 提供靜態（非影像）內容
solution: Experience Manager
title: 提供靜態（非影像）內容
topic: Scene7 Image Serving - Image Rendering API
uuid: 4ec483fe-68a4-4ae2-b5ce-730229a9bc15
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 提供靜態（非影像）內容{#serving-static-non-image-content}

「影像伺服」提供管理型錄中非影像內容的機制，並透過個別的裝置提供 `context /is/content`。 該機制允許分別配置每個項的TTL。

## 基本語法 {#section-a986baaca8644d04bcd0ddf781ae916e}

<table id="simpletable_4A6249F0C40747339524323EB0831CE4"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 請 <span class="varname"> 求 </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> http:// <span class="varname"> Server </span>/is/content[/ catalog <span class="varname"> / </span>item <span class="varname"></span>[? <span class="varname"> 修飾 </span>詞 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 伺服器 </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address </span>[: <span class="varname"> 埠 </span>] </span> </p> </td> 
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

## 命令概述 {#section-61657a0141914053ab12038ad7e91500}

「影像伺服」支援下列/is/content命令：

<table id="simpletable_1D96BA1AB5394B3C9B91D46617AFC0FA"> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" type="reference" format="dita" scope="local"> 類型 </a> </td> 
  <td class="stentry"> <p>內容類型篩選。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> requin </a> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>、 <span class="codeph"> req=props </span>和req=exists <span class="codeph"></span> only. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" type="reference" format="dita" scope="local"> 快取 </a> </td> 
  <td class="stentry"> <p>允許禁用客戶端快取。 </p> </td> 
 </tr> 
</table>

## 靜態內容目錄 {#section-b2b8f4860fe84e528493ed704c7c5141}

靜態內容目錄類似於影像目錄，但支援的資料欄位較少：

<table id="table_3B111EC3AA1044FB9B659FD54BADDC39"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 屬性／資料</b> </th> 
   <th class="entry"> <b> 附註</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 目錄：:Id </span> </p> </td> 
   <td> <p> 此靜態內容項目的目錄記錄標識符 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 目錄：：路徑 </span> </p> </td> 
   <td> <p> 此內容項的檔案路徑 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 目錄：：過期 </span> </p> </td> 
   <td> <p> 此內容項目的TTL;屬性：：如果未指定或空白，則使用過期 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 目錄：:TimeStamp </span> </p> </td> 
   <td> <p> 檔案修改時間戳；啟用屬性：:CacheValidationPolicy時所需的 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 目錄：:UserData </span> </p> </td> 
   <td> <p> 與此靜態內容項目相關的可選元資料；可用於具有req=userdata的客戶端 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 目錄：:UserType </span> </p> </td> 
   <td> <p> 可選資料類型；可用於使用type=命令篩選靜態內容的請求 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 篩選靜態內容 {#section-896c37cf68bc446eb0766fb378898262}

此機制可協助確保用戶端只收到符合其需求的內容。 假設靜態內容標籤了適當的 `catalog::UserType`值，客戶端可以將命 `type=` 令添加到請求中。 「影像伺服」會比較命令所提供 `type=` 的值與值，並 `catalog::UserType` 在發生不相符的情況下，傳回錯誤，而非可能不適當的內容。

## 另請參閱 {#section-91c7b686aacf4d3ca974f35a3fe3d6ec}

[type=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)，影像目錄 [參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
