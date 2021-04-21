---
description: 資產的可擴充中繼資料平台關鍵字。
solution: Experience Manager
title: XmpKeywords
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 18%

---


# XmpKeywords{#xmpkeywords}

資產的可擴充中繼資料平台關鍵字。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名稱 </th> 
   <th colname="col2" class="entry"> 類型 </th> 
   <th colname="col3" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 項目</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>以逗號分隔的關鍵字清單，可合併至<span class="codeph"> dc:subject=</span>屬性節XMP點。 如果逗號出現在任何個別值中，則需要以反斜線(\)字元逸出逗號。 如果是常值反斜線，則使用一般的雙反斜線 (\\)。 </p> </td> 
  </tr> 
 </tbody> 
</table>

