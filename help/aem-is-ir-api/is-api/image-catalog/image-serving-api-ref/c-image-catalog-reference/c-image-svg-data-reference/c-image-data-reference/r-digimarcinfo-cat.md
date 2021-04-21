---
description: Digimarc影像資訊。 啟用Digimarc嵌入並指定水印類型和任何關聯的特定影像資料。
solution: Experience Manager
title: DigimarcInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 14%

---


# DigimarcInfo{#digimarcinfo}

Digimarc影像資訊。 啟用Digimarc嵌入並指定水印類型和任何關聯的特定影像資料。

## 屬性 {#section-62af219e8bac422b8541841221c9ce4f}

四個整數值，以逗號分隔。

`*``*, *``*, *`typeflagsval1`*, *`val2`*`

`*``*` typeenables Digimarc embedding and specification the watermark type:

<table id="table_3648951F14D94C5BAD097CFB783F1EE7"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> type</span> </span> </p> </th> 
   <th class="entry"> <p><b>水印類型</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>無。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>基本. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>影像 ID. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>交易 ID. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>版權年份。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`*`標`*` 記具有三個值的位欄位。設定位元0以表示受複製保護的內容，設定位元1以表示受限制的內容，設定位元2以表示成人內容：

<table id="table_00F218515FBE484F9D05CBAF14F9D045"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> 旗標</span> </span> </p> </th> 
   <th class="entry"> <p><b>說明</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>- </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>受複製保護。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>受限制。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>受複製保護，受限制。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>成熟的內容。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>5</b> </p> </td> 
   <td> <p>複製受保護的成人內容。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>6</b> </p> </td> 
   <td> <p>限制性的成人內容。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>7</b> </p> </td> 
   <td> <p>受複製保護、受限制、成熟的內容。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`*`val1`*`和`*`val2`*`的解釋取決於`*`type`*`:

<table id="table_6B29F76BC1974C12AB7124BF84B29EC2"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> type</span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val1  </span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val2  </span> </span> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>未使用。 </p> </td> 
   <td> <p>未使用。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>未使用。 </p> </td> 
   <td> <p>未使用。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>影像 ID. </p> </td> 
   <td> <p>未使用。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>交易 ID. </p> </td> 
   <td> <p>未使用。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>首年版權。 </p> </td> 
   <td> <p>第二個版權年。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 預設 {#section-4bb97e5f79074be89cc691e73449eb43}

繼承自屬性：:DigimarcInfo（如果欄位不存在或為空）。

## 範例 {#section-0f14727a0a2a408781c9df71fed7f42d}

「0,0,0,0」會停用此影像的Digimarc浮水印。

&quot;1,5,0,0&quot;會指定設定成人與受複製保護內容旗標的基本浮水印。

&quot;2,0,4567,0&quot;指定具有影像ID的水印。

&quot;3,2,56483,0&quot;指定具有交易ID和限制內容標幟集的浮水印。

&quot;4,0,1998,2001&quot;指定具有版權年的水印。

## 另請參閱 {#section-4bd3e7272c5c4b8cb8c5ca1ac7ed1012}

[屬性：:DigimarcInfo](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcinfo.md#reference-de88636cb9b4435a94e3d0a80f072667) ，屬 [性：:DigimarcId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcid.md#reference-33e3eca7f1874510904e5c8645cecd68)
