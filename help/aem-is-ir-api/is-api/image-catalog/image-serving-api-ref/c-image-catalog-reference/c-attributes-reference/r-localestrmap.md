---
description: 字串轉譯映射。 指可映射至任何數目internalLocId的locId。
seo-description: 字串轉譯映射。 指可映射至任何數目internalLocId的locId。
seo-title: LocaleStrMap
solution: Experience Manager
title: LocaleStrMap
topic: Scene7 Image Serving - Image Rendering API
uuid: 44207916-80a6-42cb-8bf1-fcf0f5194c6d
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# LocaleStrMap{#localestrmap}

字串轉譯映射。 指可映射至任何數目internalLocId的locId。

` *`itemitem`*&#42;['|' *``*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 項目 </span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> locale </span>, <span class="varname"> locId </span>*[',' <span class="varname"> locId </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 地區設定 </span> </p> </td> 
  <td class="stentry"> <p>地區設定（不區分大小寫）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId </span> </p> </td> 
  <td class="stentry"> <p>內部地區ID。 </p> </td> 
 </tr> 
</table>

`LocaleStrMap` 是指可 `locId` 以映射至任意數目的 `internalLocId`。

空值與空 *`locale`* 字串和未知的字串相 `locale=` 符。 這允許為未知地區設定定義預設規則。

允許 *`locId`* 使用空值並選擇 *`defaultString`* (不 *`defaultString`* 具有地區識別碼)。 *`locId`* 值會依指定順序搜尋。 會傳回第一個相符項目。

字串轉換在啟用時，會套用至下列影像目錄欄位中的文字字串：

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>目錄欄位</b> </td> 
   <td> <b>欄位中的字串元素</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 目錄：:ImageSet </span> </p> </td> 
   <td> <p>任何包含可翻譯字串的子元素（由分隔符',' ';' ':'和／或欄位開始／結束的任意組合所分隔）。 </p> <p>在可 <span class="codeph"> 本地化 </span> 欄位的開頭處的0xrrggbb顏色值被排除在本地化之外，並且不經修改而通過。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 目錄：:Map </span> </p> </td> 
   <td> <p>任何單引號或雙引號屬性值，但coords= <span class="codeph"> 和shape=屬 </span> 性 <span class="codeph"> 的值除外 </span> 。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 目錄：：目標 </span> </p> </td> 
   <td> <p>任何目標的 <span class="filepath"> 值。*.label </span> 和目 <span class="filepath"> 標。*.userdata屬 </span> 性。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 目錄：:UserData </span> </p> </td> 
   <td> <p>任何屬性的值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-8505a8525f6948ada3979f68c4081044}

一或多個項目，以|，其中每個項目包含兩個或更多個逗號分隔的字串值。

## 另請參閱 {#section-0c0516e4f83d42d38247308cab9b6708}

本地化支 [持區域設定=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb)，屬性：:LocaleMap [，目錄：:ImageSet](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318)，目錄：目錄： [](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md)[](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md)[](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md)[Map，目錄：目標：目錄：目錄：用戶資料：目錄](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
