---
description: 請求規則元素。 在 <ruleset> 的子菜單。
solution: Experience Manager
title: 規則
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8f56012c-d01c-489c-9d18-91e256f72012
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 5%

---

# 規則{#rule}

請求規則元素。 在 `<ruleset>` 的子菜單。

## 屬性 {#section-aa23349645434db99d46957a96f2e1e1}

`OnMatch="break"|"continue"|"error"` 選擇性. 預設值為&quot;break&quot;。

` Name=" *`文本`*"` 可選。 用於標識 `<rule>` 調試日誌和錯誤消息中的元素。

另外， `<rule>` 元素可以在任何組合中定義以下任何屬性。 如果指定，並且規則成功匹配，則它們將覆蓋此請求的相應目錄屬性。

<table id="table_AFEFDE61C9ED40019C10D8FE5B16CA23"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>&lt;rule&gt; 屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>相應的影像目錄屬性 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 預設影像 </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f" type="reference" format="dita" scope="local"> 屬性：:DefautPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 錯誤影像 </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0" type="reference" format="dita" scope="local"> 屬性：:ErrorImage </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 過期 </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996" type="reference" format="dita" scope="local"> 屬性：：到期 </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 最大圖 </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657" type="reference" format="dita" scope="local"> 屬性：:MaxPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 根URL </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402" type="reference" format="dita" scope="local"> 屬性：:RootUrl </a> </p> </td> 
  </tr> 
 </tbody> 
</table>

有關詳細資訊，請參閱相應影像目錄屬性的說明。

「到期」屬性僅覆蓋預設屬性值；如果特定 `catalog::Expiration` 值適用於請求。

## 資料 {#section-401b6dfce082490f81229a19b73f2562}

<table id="simpletable_A7E17B52AF754687ACCFFBE747939331"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;expression&gt; </span> </p> </td> 
  <td class="stentry"> <p>選擇性. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;substitution&gt; </span> </p> </td> 
  <td class="stentry"> <p>選擇性. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;addressfilter&gt; </span> </p> </td> 
  <td class="stentry"> <p>選擇性. </p> </td> 
 </tr> 
</table>

## 附註 {#section-a27b91f9a03047c0bb7edc0967fb4216}

如果兩者都 `<expression>` 和 `<substitution>` 指定，且不使用捕獲的子字串，則第一個匹配的子字串將替換為 `<substitution>`。

如果 `<expression>` 未指定，任何路徑將匹配， `<substitution>` 添加到路徑的末尾。

如果 `<substitution>` 未指定，將刪除匹配的子字串。

的 `<addressfilter>` 僅在出現匹配時和應用查詢規則之前應用。
