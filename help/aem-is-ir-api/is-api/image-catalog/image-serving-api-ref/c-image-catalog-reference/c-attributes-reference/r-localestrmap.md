---
description: 字串轉換映射。 引用可映射到任意數目的internalLocId的locId。
solution: Experience Manager
title: 區域設定字串映射
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48a1c71c-78a9-43db-8b1a-4189d34b0982
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 1%

---

# 區域設定字串映射{#localestrmap}

字串轉換映射。 引用可映射到任意數目的internalLocId的locId。

`*`物料`*&#42;['|' *`物料`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 項目 </span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> 區域 </span>。 <span class="varname"> locId </span>*[',' <span class="varname"> locId </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 地區設定 </span> </p> </td> 
  <td class="stentry"> <p>區域設定（不區分大小寫）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId </span> </p> </td> 
  <td class="stentry"> <p>內部區域設定ID。 </p> </td> 
 </tr> 
</table>

`LocaleStrMap` 是指 `locId` 可以映射到任意數量 `internalLocId`。

空 *`locale`* 值與空匹配，未知 `locale=` 字串。 這允許為未知區域設定定義預設規則。

空 *`locId`* 允許的值，並選擇 *`defaultString`* ( *`defaultString`* 沒有區域設定標識符)。 *`locId`* 按指定的順序搜索值。 返回第一個匹配。

啟用字串轉換後，將應用於以下影像目錄欄位中的文本字串：

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>目錄欄位</b> </td> 
   <td> <b>欄位中的字串元素</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 目錄：:ImageSet </span> </p> </td> 
   <td> <p>包含可翻譯字串的任何子元素（由分隔符「，」「；」「：」和/或欄位的開始/結束的任意組合分隔）。 </p> <p>A <span class="codeph"> 0xrgbb </span> 可本地化欄位開頭的顏色值被排除在本地化之外，並且不經修改而通過。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 目錄：：映射 </span> </p> </td> 
   <td> <p>任何單引號或雙引號的屬性值， <span class="codeph"> 坐標= </span> 和 <span class="codeph"> 形狀= </span> 屬性。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 目錄：：目標 </span> </p> </td> 
   <td> <p>任何值 <span class="filepath"> 目標。*.label </span> 和 <span class="filepath"> 目標。*.用戶資料 </span> 屬性。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 目錄：:UserData </span> </p> </td> 
   <td> <p>任何屬性的值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-8505a8525f6948ada3979f68c4081044}

一個或多個項目，以 |，其中每個項包含兩個或更多以逗號分隔的字串值。

## 另請參閱 {#section-0c0516e4f83d42d38247308cab9b6708}

本地化支援、 [區域設定=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb)。 [屬性：:LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318)。 [目錄：:ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md)。 [目錄：：映射](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md)。 [目錄：：目標](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md)。 [目錄：:UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
