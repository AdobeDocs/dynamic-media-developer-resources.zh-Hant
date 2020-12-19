---
description: 將中繼資料發佈至中繼資料伺服器。
seo-description: 將中繼資料發佈至中繼資料伺服器。
seo-title: MetadataPublishJobType
solution: Experience Manager
title: MetadataPublishJobType
topic: Scene7 Image Production System API
uuid: 14cbb67e-56dc-4a25-b871-740be7ea7858
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '72'
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

