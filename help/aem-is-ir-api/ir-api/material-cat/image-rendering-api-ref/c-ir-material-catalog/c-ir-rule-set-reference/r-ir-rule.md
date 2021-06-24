---
description: 要求規則元素。 在<規則集>元素中，有一或多個是可選的。
solution: Experience Manager
title: 規則
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 8f56012c-d01c-489c-9d18-91e256f72012
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 5%

---

# 規則{#rule}

要求規則元素。 `<ruleset>`元素中有一或多個是選用項目。

## 屬性 {#section-aa23349645434db99d46957a96f2e1e1}

`OnMatch="break"|"continue"|"error"`選填。預設為「break」。

` Name=" *``*"` textOptional。用於識別除錯記錄和錯誤訊息中的`<rule>`元素。

此外，`<rule>`元素可以在任何組合中定義以下任何屬性。 如果已指定且規則已成功符合，則會覆寫此請求的對應目錄屬性。

<table id="table_AFEFDE61C9ED40019C10D8FE5B16CA23"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>&lt;rule&gt; 屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>對應的影像目錄屬性 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> DefaultPix  </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f" type="reference" format="dita" scope="local"> 屬性：:DefautPix  </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ErrorImage  </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0" type="reference" format="dita" scope="local"> 屬性：:ErrorImage  </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 過期 </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996" type="reference" format="dita" scope="local"> 屬性：：過期  </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MaxPix  </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657" type="reference" format="dita" scope="local"> 屬性：:MaxPix  </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RootUrl  </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402" type="reference" format="dita" scope="local"> 屬性：:RootUrl  </a> </p> </td> 
  </tr> 
 </tbody> 
</table>

如需詳細資訊，請參閱對應影像目錄屬性的說明。

Expiration屬性只覆蓋預設屬性值；如果特定`catalog::Expiration`值套用至請求，則會忽略此值。

## 資料 {#section-401b6dfce082490f81229a19b73f2562}

<table id="simpletable_A7E17B52AF754687ACCFFBE747939331"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;expression&gt; </span> </p> </td> 
  <td class="stentry"> <p>選填。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;substitution&gt; </span> </p> </td> 
  <td class="stentry"> <p>選填。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;addressfilter&gt; </span> </p> </td> 
  <td class="stentry"> <p>選填。 </p> </td> 
 </tr> 
</table>

## 附註 {#section-a27b91f9a03047c0bb7edc0967fb4216}

如果同時指定了`<expression>`和`<substitution>`，並且未使用捕獲的子字串，則第一個匹配的子字串將替換為`<substitution>`。

如果未指定`<expression>`，則任何路徑都將匹配，並且`<substitution>`將附加到路徑的結尾。

如果未指定`<substitution>`，則刪除匹配的子字串。

`<addressfilter>`僅在發生匹配時應用，並在應用查詢規則之前應用。
