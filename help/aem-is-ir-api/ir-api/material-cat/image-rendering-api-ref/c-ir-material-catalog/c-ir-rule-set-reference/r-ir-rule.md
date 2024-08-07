---
description: 要求規則元素。 <ruleset>元素中有一或多個是選用專案。
solution: Experience Manager
title: 規則
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8f56012c-d01c-489c-9d18-91e256f72012
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 4%

---

# 規則{#rule}

要求規則元素。 `<ruleset>`專案中的一或多個為選用專案。

## 屬性 {#section-aa23349645434db99d46957a96f2e1e1}

`OnMatch="break"|"continue"|"error"`選擇性。 預設值為「break」。

` Name=" *`文字`*"`選擇性。 用於識別偵錯記錄檔和錯誤訊息中的`<rule>`專案。

此外，`<rule>`元素可以任意組合定義下列任何屬性。 如果已指定，且規則已成功比對，則會覆寫此請求對應的目錄屬性。

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
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f" type="reference" format="dita" scope="local">屬性：：DefautPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ErrorImage </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0" type="reference" format="dita" scope="local">屬性：：ErrorImage </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">到期</span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996" type="reference" format="dita" scope="local">屬性：：到期</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MaxPix </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657" type="reference" format="dita" scope="local">屬性：：MaxPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RootUrl </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402" type="reference" format="dita" scope="local">屬性：：RootUrl </a> </p> </td> 
  </tr> 
 </tbody> 
</table>

如需詳細資訊，請參閱對應影像目錄屬性的說明。

Expiration屬性只會覆寫預設屬性值；如果特定的`catalog::Expiration`值套用至要求，則會忽略該屬性。

## 資料 {#section-401b6dfce082490f81229a19b73f2562}

<table id="simpletable_A7E17B52AF754687ACCFFBE747939331"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;運算式&gt; </span> </p> </td> 
  <td class="stentry"> <p>選擇性. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;替代&gt; </span> </p> </td> 
  <td class="stentry"> <p>選擇性. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;addressfilter&gt; </span> </p> </td> 
  <td class="stentry"> <p>選擇性. </p> </td> 
 </tr> 
</table>

## 附註 {#section-a27b91f9a03047c0bb7edc0967fb4216}

如果同時指定`<expression>`和`<substitution>`，但未使用擷取的子字串，則第一個相符的子字串會取代為`<substitution>`。

如果未指定`<expression>`，則所有路徑皆相符，且`<substitution>`會附加至路徑的結尾。

如果未指定`<substitution>`，則會移除相符的子字串。

`<addressfilter>`只會在符合發生時套用，並在套用查詢規則之前套用。
