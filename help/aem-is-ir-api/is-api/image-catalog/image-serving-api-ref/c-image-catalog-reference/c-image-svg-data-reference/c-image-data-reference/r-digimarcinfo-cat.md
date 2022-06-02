---
title: DigimarcInfo
description: Digimarc影像資訊。 啟用Digimarc嵌入，並指定水印類型和任何關聯的影像特定資料。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 87f4d8f0-02b9-4511-9151-89c58116c78d
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 14%

---

# DigimarcInfo{#digimarcinfo}

Digimarc影像資訊。 啟用Digimarc嵌入，並指定水印類型和任何關聯的影像特定資料。

## 屬性 {#section-62af219e8bac422b8541841221c9ce4f}

四個整數值，用逗號分隔。

`*`類型`*, *`標誌`*, *`val1`*, *`val2`*`

`*`類型`*` 啟用Digimarc嵌入並指定水印類型：

<table id="table_3648951F14D94C5BAD097CFB783F1EE7"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> 類型</span> </span> </p> </th> 
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

`*`標誌`*` 是具有三個值的位欄位。 將位0設定為指示受複製保護的內容，將位1設定為指示受限內容，將位2設定為指示成人內容：

<table id="table_00F218515FBE484F9D05CBAF14F9D045"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> 標誌</span> </span> </p> </th> 
   <th class="entry"> <p><b>說明</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>- </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>受複製保護。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>限制。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>受複製保護，受限。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>成熟內容。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>5</b> </p> </td> 
   <td> <p>複製受保護的成人內容。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>6</b> </p> </td> 
   <td> <p>限制，成人內容。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>7</b> </p> </td> 
   <td> <p>受拷貝保護、受限、成熟的內容。 </p> </td> 
  </tr> 
 </tbody> 
</table>

對 `*`val1`*` 和 `*`val2`*` 依靠 `*`類型`*`:

<table id="table_6B29F76BC1974C12AB7124BF84B29EC2"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> 類型</span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val1 </span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val2 </span> </span> </p> </th> 
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
   <td> <p><b>3</b> </p> </td> 
   <td> <p>交易 ID. </p> </td> 
   <td> <p>未使用。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>第一個版權年。 </p> </td> 
   <td> <p>第二個版權年。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 預設 {#section-4bb97e5f79074be89cc691e73449eb43}

從屬性：:DigimarcInfo繼承（如果欄位不存在或為空）。

## 範例 {#section-0f14727a0a2a408781c9df71fed7f42d}

「0,0,0,0」禁用此影像的Digimarc水印。

「1,5,0,0」指定基本水印，並設定成人和受複製保護的內容標誌。

&quot;2,0,4567,0&quot;指定具有影像ID的水印。

&quot;3,2,56483,0&quot;指定具有事務ID和限制內容標誌集的水印。

「4,0,1998,2001」指定具有版權年的水印。

## 另請參閱 {#section-4bd3e7272c5c4b8cb8c5ca1ac7ed1012}

[屬性：:DigimarcInfo](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcinfo.md#reference-de88636cb9b4435a94e3d0a80f072667) 。 [屬性：:DigimarcId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcid.md#reference-33e3eca7f1874510904e5c8645cecd68)
