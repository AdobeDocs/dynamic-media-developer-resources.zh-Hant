---
description: ID轉換映射。 指定將一般影像ID轉換為地區特定ID的規則。
seo-description: ID轉換映射。 指定將一般影像ID轉換為地區特定ID的規則。
seo-title: LocaleMap
solution: Experience Manager
title: LocaleMap
topic: Scene7 Image Serving - Image Rendering API
uuid: 3609a595-2948-43a4-ba8c-fd1a9ea4e26e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# LocaleMap{#localemap}

ID轉換映射。 指定將一般影像ID轉換為地區特定ID的規則。

` *`itemitem`*&#42;['|' *``*]`

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
  <td class="stentry"> <p>地區字尾。 </p></td> 
 </tr> 
</table>

`LocaleMap` 是指可 `locId` 以映射至任意數目的 `locSuffix`。

Empty *`locSuffix`* values are permitted. *`locSuffix`* 值必須按照搜索順序進行排序。 會傳回第一個相符項目。

「影像伺服」 *`locId`* 會搜尋與請求中指定的值不區分大小寫 `locale=` 的相符項目。 如果找到相符項目，第一個相 *`locSuffix`* 關值會附加至原始目錄ID。 如果存在此目錄條目，則使用它，否則將嘗 *`locSuffix`* 試下一個值。 如果沒有任何值 *`locSuffix`* 與目錄條目匹配，則「影像服務」返回錯誤或預設影像。

空值與空 *`locId`* 字串和未知的字串相 `locale=` 符。 這允許為未知地區設定定義預設規則。

啟用ID轉譯後，會套用至參照影像目錄和靜態內容目錄項目的所有ID。

## 屬性 {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

一或多個項目，以|，其中每個項目包含兩個或更多個逗號分隔的字串值。 *`locId`* 並進 `locale=` 行比較。 不區分大小寫。

## 另請參閱 {#section-19fba6d5be59439c8bf8ec7513c1a6da}

本地化支 [持，locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb)，屬 [性：:LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
