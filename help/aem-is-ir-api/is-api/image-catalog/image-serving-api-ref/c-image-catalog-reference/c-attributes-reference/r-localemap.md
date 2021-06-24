---
description: ID翻譯對映。 指定用於將一般影像ID轉換為地區特定ID的規則。
solution: Experience Manager
title: LocaleMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: c1d74154-721b-46cc-9f0b-8dae5647b179
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 1%

---

# LocaleMap{#localemap}

ID翻譯對映。 指定用於將一般影像ID轉換為地區特定ID的規則。

`*``*&#42;['|' *`itemitem`*]`

<table id="simpletable_A6DD1A28F8ED4178A8ADDB2F3AEFC402"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 項目</span> </p></td> 
  <td class="stentry"> <p><span class="varname"> locId</span>,<span class="varname"> locSuffix</span>*[','<span class="varname"> locSuffix</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locId</span> </p></td> 
  <td class="stentry"> <p>地區ID（不區分大小寫）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locSuffix</span> </p></td> 
  <td class="stentry"> <p>地區尾碼。 </p></td> 
 </tr> 
</table>

`LocaleMap` 是指可 `locId` 對應至任何數量的 `locSuffix`。

允許空&#x200B;*`locSuffix`*&#x200B;值。 *`locSuffix`* 值必須按照搜索順序排序。會傳回第一個相符項目。

「影像伺服」會搜尋&#x200B;*`locId`*&#x200B;值，以找出與請求中指定的`locale=`值不區分大小寫的相符項目。 如果找到相符項目，則第一個相關聯的&#x200B;*`locSuffix`*&#x200B;值會附加至原始目錄ID。 如果此目錄項存在，則會使用它，否則會嘗試下一個&#x200B;*`locSuffix`*&#x200B;值。 如果&#x200B;*`locSuffix`*&#x200B;值中沒有一個與目錄項匹配，則「影像伺服」返回錯誤或預設影像。

空的&#x200B;*`locId`*&#x200B;值與空的和未知的`locale=`字串相符。 這允許為未知地區設定定義預設規則。

啟用ID轉譯後，會套用至參考影像目錄和靜態內容目錄項目的所有ID。

## 屬性 {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

一或多個項目，以 |，其中每個項目包含兩個或多個逗號分隔字串值。 *`locId`* 和 `locale=` 比較。不區分大小寫。

## 另請參閱 {#section-19fba6d5be59439c8bf8ec7513c1a6da}

本地化支援， [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
