---
description: 將中繼資料發佈至中繼資料伺服器。
solution: Experience Manager
title: MetadataPublishJobType
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 9%

---


# MetadataPublishJobType{#metadatapublishjobtype}

將中繼資料發佈至中繼資料伺服器。

語法

## 參數 {#section-6c51fa689b3648fbb7c7945a7e176d0a}

<table id="table_23B5CFC5C3F946F9AFDB6A83A1AAB7AF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名稱 </th> 
   <th colname="col2" class="entry"> 類型 </th> 
   <th colname="col3" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> forcePublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">設為<span class="codeph"> True</span>，以再次將<i>所有</i>資料發佈至中繼資料伺服器。 <p>注意： 視資料量而定，這可能需要幾分鐘到幾小時。 </p><p>如果您只想發佈新的或變更的中繼資料，請勿設定此參數。 </p></td> 
  </tr> 
 </tbody> 
</table>

