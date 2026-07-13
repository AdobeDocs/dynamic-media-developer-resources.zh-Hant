---
description: 選擇性型別，可讓您選擇特定視訊影格做為縮圖影像。
solution: Experience Manager
title: 縮圖選項
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7d84590d-2227-4d9a-9cb0-0f4b1fcabd8e
TQID: 'https://experienceleague.adobe.com/jwSdazwO-DxdDktvMfk7jC3Os3YL5IkE6hyi-eKwaoE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 94
ht-degree: 6%

---

# [!DNL ThumbnailOptions]{#thumbnailoptions}

選擇性型別，可讓您選擇特定視訊影格做為縮圖影像。

語法

## 參數 {#section-b1777bf868764a7099d4a954b471856c}

<table id="table_C71FD0C995D94CE18994CDA2DC3460DF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名稱 </th> 
   <th colname="col2" class="entry"> 類型 </th> 
   <th colname="col3" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">縮圖時間</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：long</span> </td> 
   <td colname="col3"> <p>針對您要用於視訊縮圖的影格，設定時間（從視訊開始算起的毫秒）。 值範圍從0到視訊結尾。 <p>注意：如果您不正確地指定時間，系統會將視訊的第一個影格用於縮圖。 請參閱<a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>。 </p></p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-ce3b59c60fea4cd4945427a025051447}

```
<complexType name="ThumbnailOptions">
     <sequence>
        <element name="thumbnailTime" type="xsd:long" minOccurs="0"/>
      </sequence>
</complexType>
```

