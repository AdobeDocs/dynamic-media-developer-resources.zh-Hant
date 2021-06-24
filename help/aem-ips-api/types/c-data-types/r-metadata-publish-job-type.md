---
description: 將元資料發佈到元資料伺服器。
solution: Experience Manager
title: MetadataPublishJobType
feature: Dynamic Media Classic,SDK/API，中繼資料
role: Developer,Administrator
exl-id: b90d27c0-9398-4597-bcce-3c36a371df22
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 9%

---

# MetadataPublishJobType{#metadatapublishjobtype}

將元資料發佈到元資料伺服器。

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
   <td colname="col3">設為<span class="codeph"> True</span> ，以再次將<i>所有</i>資料發佈到中繼資料伺服器。 <p>注意： 視資料量而定，這可能需要幾分鐘到數小時。 </p><p>如果您只想發佈新的或已變更的中繼資料，請勿設定此參數。 </p></td> 
  </tr> 
 </tbody> 
</table>
