---
description: 字串轉譯映射。 指可映射至任何數目internalLocId的locId。
solution: Experience Manager
title: LocaleStrMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 2%

---


# LocaleStrMap{#localestrmap}

字串轉譯映射。 指可映射至任何數目internalLocId的locId。

`*`itemitem`*&#42;['|' *``*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 項目 </span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> locale  </span>,  <span class="varname"> locId  </span>*[','  <span class="varname"> locId  </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 地區設定 </span> </p> </td> 
  <td class="stentry"> <p>地區設定（不區分大小寫）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId  </span> </p> </td> 
  <td class="stentry"> <p>內部地區ID。 </p> </td> 
 </tr> 
</table>

`LocaleStrMap` 是指可 `locId` 以映射至任意數目的 `internalLocId`。

空的&#x200B;*`locale`*&#x200B;值與空的和未知的`locale=`字串匹配。 這允許為未知地區設定定義預設規則。

允許空&#x200B;*`locId`*&#x200B;值，並選擇&#x200B;*`defaultString`*（*`defaultString`*&#x200B;沒有地區標識符）。 *`locId`* 值會依指定順序搜尋。會傳回第一個相符項目。

字串轉換在啟用時，會套用至下列影像目錄欄位中的文字字串：

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>目錄欄位</b> </td> 
   <td> <b>欄位中的字串元素</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 目錄：:ImageSet  </span> </p> </td> 
   <td> <p>任何包含可翻譯字串的子元素（由分隔符',' ';' ':'和／或欄位開始／結束的任意組合所分隔）。 </p> <p>在可本地化欄位的開頭處的<span class="codeph"> 0xrrgbb </span>顏色值被排除在本地化之外，並且不經修改而通過。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 目錄：:Map  </span> </p> </td> 
   <td> <p>除<span class="codeph"> coords= </span>和<span class="codeph"> shape= </span>屬性的值外，任何單引號或雙引號屬性值。 </p> </td> 
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

一或多個項目，以 |，其中每個項目包含兩個或更多個逗號分隔的字串值。

## 另請參閱 {#section-0c0516e4f83d42d38247308cab9b6708}

本地化支援，[locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb),[屬性：:LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318),[目錄：:ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md),[目錄：Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md),[目錄：Targets](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md),[目錄：userData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
