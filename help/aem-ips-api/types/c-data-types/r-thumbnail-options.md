---
description: 可選類型，可讓您選擇特定視訊影格做為縮圖影像。
seo-description: 可選類型，可讓您選擇特定視訊影格做為縮圖影像。
seo-title: ThumbnailOptions
solution: Experience Manager
title: ThumbnailOptions
uuid: 50b2ecee-8396-4323-83e1-1f5060bec6c4
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 5%

---


# ThumbnailOptions{#thumbnailoptions}

可選類型，可讓您選擇特定視訊影格做為縮圖影像。

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbnailTime</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> <p>設定您要用於視訊縮圖的影格的時間（從視訊開始以毫秒為單位）。 值範圍從0到視訊結尾。 <p>注意：如果您未正確指定時間，系統會將視訊的第一個影格用於縮圖。 請參閱<a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>。 </p></p> </td> 
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

