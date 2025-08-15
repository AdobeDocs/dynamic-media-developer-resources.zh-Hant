---
description: ID轉譯對應。 指定用於將一般影像ID轉譯為地區設定特定ID的規則。
solution: Experience Manager
title: LocaleMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c1d74154-721b-46cc-9f0b-8dae5647b179
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# LocaleMap{#localemap}

ID轉譯對應。 指定用於將一般影像ID轉譯為地區設定特定ID的規則。

`*`專案`*&#42;['|' *`專案`*]`

<table id="simpletable_A6DD1A28F8ED4178A8ADDB2F3AEFC402"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">專案</span> </p></td> 
  <td class="stentry"> <p><span class="varname"> locId</span>，<span class="varname"> locSuffix</span>*['，'<span class="varname"> locSuffix</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locId</span> </p></td> 
  <td class="stentry"> <p>地區設定ID （不區分大小寫）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locSuffix</span> </p></td> 
  <td class="stentry"> <p>地區設定尾碼。 </p></td> 
 </tr> 
</table>

`LocaleMap`參考可對應至任意數量的`locId`的`locSuffix`。

允許空的&#x200B;*`locSuffix`*&#x200B;值。 *`locSuffix`*&#x200B;值必須依搜尋它們的順序排序。 會傳回第一個相符專案。

「影像伺服」會搜尋&#x200B;*`locId`*&#x200B;值，找出與要求中所指定`locale=`值相符且不區分大小寫的相符專案。 如果找到相符專案，第一個關聯的&#x200B;*`locSuffix`*&#x200B;值會附加至原始目錄ID。 如果此目錄專案存在，則會使用它，否則會嘗試下一個&#x200B;*`locSuffix`*&#x200B;值。 如果&#x200B;*`locSuffix`*&#x200B;個值都不符合目錄專案，「影像伺服」會傳回錯誤或預設影像。

空白&#x200B;*`locId`*&#x200B;值與空白和未知`locale=`字串相符。 這允許為未知的區域設定定義預設規則。

ID轉譯在啟用時，會套用至參考影像目錄和靜態內容目錄專案的所有ID。

## 屬性 {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

一或多個專案，以分隔 |，其中每個專案都包含兩個或多個以逗號分隔的字串值。 已比較&#x200B;*`locId`*&#x200B;與`locale=`。 不區分大小寫。

## 另請參閱 {#section-19fba6d5be59439c8bf8ec7513c1a6da}

本地化支援，[locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb)，[attribute：：LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
