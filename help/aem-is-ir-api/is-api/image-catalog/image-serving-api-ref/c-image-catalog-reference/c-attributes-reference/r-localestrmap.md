---
description: 字串轉換映射。 指可對應至任何數量之internalLocId的locId。
solution: Experience Manager
title: LocaleStrMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 48a1c71c-78a9-43db-8b1a-4189d34b0982
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 2%

---

# LocaleStrMap{#localestrmap}

字串轉換映射。 指可對應至任何數量之internalLocId的locId。

`*``*&#42;['|' *`itemitem`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 項目 </span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> locale  </span>,  <span class="varname"> locId  </span>*[','  <span class="varname"> locId  </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 地區設定 </span> </p> </td> 
  <td class="stentry"> <p>地區（不區分大小寫）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId  </span> </p> </td> 
  <td class="stentry"> <p>內部地區ID。 </p> </td> 
 </tr> 
</table>

`LocaleStrMap` 是指可 `locId` 對應至任何數量的 `internalLocId`。

空的&#x200B;*`locale`*&#x200B;值與空的和未知的`locale=`字串相符。 這允許為未知地區設定定義預設規則。

允許空&#x200B;*`locId`*&#x200B;值，並選擇&#x200B;*`defaultString`*（*`defaultString`*&#x200B;沒有區域設定標識符）。 *`locId`* 會依指定順序搜尋值。會傳回第一個相符項目。

字串轉譯（若已啟用）會套用至下列影像目錄欄位中的文字字串：

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>目錄欄位</b> </td> 
   <td> <b>欄位中的字串元素</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 目錄：:ImageSet  </span> </p> </td> 
   <td> <p>任何包含可翻譯字串的子元素（由分隔符號「，」「；」「：」和/或欄位的開始/結束的任何組合所分隔）。 </p> <p>本地化欄位開頭的<span class="codeph"> 0xrrggbb </span>顏色值被排除在本地化之外，並且不經修改而傳遞。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 目錄：:Map  </span> </p> </td> 
   <td> <p>任何單引號或雙引號屬性值，但<span class="codeph"> coords= </span>和<span class="codeph"> shape= </span>屬性的值除外。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 目錄：：目標  </span> </p> </td> 
   <td> <p>任何<span class="filepath">目標的值。*.label </span>和<span class="filepath">目標。*.userdata </span>屬性。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 目錄：:UserData  </span> </p> </td> 
   <td> <p>任何屬性的值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-8505a8525f6948ada3979f68c4081044}

一或多個項目，以 |，其中每個項目包含兩個或多個以逗號分隔的字串值。

## 另請參閱 {#section-0c0516e4f83d42d38247308cab9b6708}

本地化支援， [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [catalog::Targets](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md), [catalog::UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
