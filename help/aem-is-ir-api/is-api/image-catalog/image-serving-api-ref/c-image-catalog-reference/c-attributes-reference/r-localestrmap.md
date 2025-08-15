---
description: 字串翻譯對應。 參考可對應至任何數量internalLocId的locId。
solution: Experience Manager
title: LocaleStrMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48a1c71c-78a9-43db-8b1a-4189d34b0982
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---

# LocaleStrMap{#localestrmap}

字串翻譯對應。 參考可對應至任何數量internalLocId的locId。

`*`專案`*&#42;['|' *`專案`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">專案</span> </p> </td> 
  <td class="stentry"> <p> <span class="varname">地區設定</span>，<span class="varname"> locId </span>*['，' <span class="varname"> locId </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">地區設定</span> </p> </td> 
  <td class="stentry"> <p>地區設定（不區分大小寫）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId </span> </p> </td> 
  <td class="stentry"> <p>內部地區設定ID。 </p> </td> 
 </tr> 
</table>

`LocaleStrMap`參考可對應至任意數量的`locId`的`internalLocId`。

空白&#x200B;*`locale`*&#x200B;值與空白和未知`locale=`字串相符。 這允許為未知的區域設定定義預設規則。

允許空白&#x200B;*`locId`*&#x200B;值，並選取&#x200B;*`defaultString`* （*`defaultString`*&#x200B;沒有地區設定識別碼）。 *`locId`*&#x200B;值會依指定的順序搜尋。 會傳回第一個相符專案。

字串轉譯在啟用時，會套用至下列影像目錄欄位中的文字字串：

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>目錄欄位</b> </td> 
   <td> 欄位<b>中的</b>字串元素 </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">目錄：：影像集</span> </p> </td> 
   <td> <p>包含可翻譯字串的任何子元素（以分隔符號「，」「；」「：」和/或欄位開頭/結尾的任何組合分隔）。 </p> <p>可當地語系化欄位開頭的<span class="codeph"> 0xrrggbb </span>色彩值會從本地化中排除，且不會經過修改而通過。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">目錄：：對應</span> </p> </td> 
   <td> <p>任何單引號或雙引號屬性值，除了<span class="codeph">字串= </span>和<span class="codeph">形狀= </span>屬性的值。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">目錄：：目標</span> </p> </td> 
   <td> <p>任何<span class="filepath">目標的值。*.label </span>和<span class="filepath">目標。*.userdata </span>屬性。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">目錄：：UserData </span> </p> </td> 
   <td> <p>任何屬性的值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-8505a8525f6948ada3979f68c4081044}

一或多個專案，以分隔 |，其中每個專案都包含兩個或多個以逗號分隔的字串值。

## 另請參閱 {#section-0c0516e4f83d42d38247308cab9b6708}

本地化支援，[地區設定=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb)，[屬性：：LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318)，[目錄：：ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md)，[目錄：：Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md)，[目錄：：Targets](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md)，[目錄：：UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
