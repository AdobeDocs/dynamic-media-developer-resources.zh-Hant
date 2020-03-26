---
description: 請求規則元素。 在<規則集>元素中有一或多個是可選的。
seo-description: 請求規則元素。 在<規則集>元素中有一或多個是可選的。
seo-title: 規則
solution: Experience Manager
title: 規則
topic: Scene7 Image Serving - Image Rendering API
uuid: f7071681-e97e-4081-aeb1-093d2b23041c
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# 規則{#rule}

請求規則元素。 元素中有一或多個是選用 `<ruleset>` 的。

## 屬性 {#section-aa23349645434db99d46957a96f2e1e1}

`OnMatch="break"|"continue"|"error"`選填。預設值為&quot;break&quot;。

` Name=" *`文字`*"` （可選）。 用於識別除錯 `<rule>` 記錄檔和錯誤訊息中的元素。

此外，元 `<rule>` 素可以在任意組合中定義下列任何屬性。 如果已指定，且規則已成功符合，則會覆寫此請求的對應目錄屬性。

<table id="table_AFEFDE61C9ED40019C10D8FE5B16CA23"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>&lt;rule&gt;屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>對應的影像目錄屬性 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> DefaultPix </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f" type="reference" format="dita" scope="local"> 屬性：:DefautPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ErrorImage </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0" type="reference" format="dita" scope="local"> 屬性：:ErrorImage </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 過期 </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996" type="reference" format="dita" scope="local"> 屬性：：到期 </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MaxPix </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657" type="reference" format="dita" scope="local"> 屬性：:MaxPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RootUrl </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402" type="reference" format="dita" scope="local"> 屬性：:RootUrl </a> </p> </td> 
  </tr> 
 </tbody> 
</table>

如需詳細資訊，請參閱對應影像目錄屬性的說明。

「到期」屬性只覆蓋預設屬性值；如果特定值套用至請 `catalog::Expiration` 求，則會忽略此值。

## 資料 {#section-401b6dfce082490f81229a19b73f2562}

<table id="simpletable_A7E17B52AF754687ACCFFBE747939331"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;expression&gt; </span> </p> </td> 
  <td class="stentry"> <p>選填。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;substitition&gt; </span> </p> </td> 
  <td class="stentry"> <p>選填。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;地址篩選器&gt; </span> </p> </td> 
  <td class="stentry"> <p>選填。 </p> </td> 
 </tr> 
</table>

## 附註 {#section-a27b91f9a03047c0bb7edc0967fb4216}

如果同時 `<expression>` 指定 `<substitution>` 和，且未使用擷取的子字串，則第一個相符的子字串會取代為 `<substitution>`。

如果 `<expression>` 未指定，則任何路徑都將匹配 `<substitution>` 並附加到路徑的末尾。

如果未 `<substitution>` 指定，則會移除相符的子字串。

只有在 `<addressfilter>` 發生符合時，以及套用查詢規則之前，才會套用。
