---
description: ID轉換映射。 指定用於將一般影像ID轉換為區域設定特定ID的規則。
solution: Experience Manager
title: 區域設定映射
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c1d74154-721b-46cc-9f0b-8dae5647b179
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 1%

---

# 區域設定映射{#localemap}

ID轉換映射。 指定用於將一般影像ID轉換為區域設定特定ID的規則。

`*`物料`*&#42;['|' *`物料`*]`

<table id="simpletable_A6DD1A28F8ED4178A8ADDB2F3AEFC402"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 項目</span> </p></td> 
  <td class="stentry"> <p><span class="varname"> locId</span>。<span class="varname"> loc尾碼</span>*[','<span class="varname"> loc尾碼</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locId</span> </p></td> 
  <td class="stentry"> <p>區域設定ID（不區分大小寫）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> loc尾碼</span> </p></td> 
  <td class="stentry"> <p>區域設定尾碼。 </p></td> 
 </tr> 
</table>

`LocaleMap` 是指 `locId` 可以映射到任意數量 `locSuffix`。

空 *`locSuffix`* 允許使用值。 *`locSuffix`* 值必須按要搜索的順序排序。 返回第一個匹配。

影像服務搜索 *`locId`* 與 `locale=` 在請求中指定的值。 如果找到匹配項，則第一個關聯項 *`locSuffix`* 值將附加到原始目錄id。 如果此目錄條目存在，則使用它，否則 *`locSuffix`* 已嘗試值。 如果 *`locSuffix`* 值與目錄項匹配，Image Serving返回錯誤或預設映像。

空 *`locId`* 值與空匹配，未知 `locale=` 字串。 這允許為未知區域設定定義預設規則。

啟用ID轉換後，將應用於所有引用影像目錄和靜態內容目錄條目的ID。

## 屬性 {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

一個或多個項目，以 |，其中每個項包含兩個或多個逗號分隔的字串值。 *`locId`* 和 `locale=` 。 不區分大小寫。

## 另請參閱 {#section-19fba6d5be59439c8bf8ec7513c1a6da}

本地化支援、 [區域設定=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb)。 [屬性：:LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
