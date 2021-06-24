---
description: 一種可選類型，可讓您選擇特定視訊影格作為縮圖影像。
solution: Experience Manager
title: ThumbnailOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 7d84590d-2227-4d9a-9cb0-0f4b1fcabd8e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 6%

---

# ThumbnailOptions{#thumbnailoptions}

一種可選類型，可讓您選擇特定視訊影格作為縮圖影像。

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
   <td colname="col3"> <p>設定您要用於視訊縮圖的影格的時間（以視訊開始的毫秒為單位）。 值範圍從0到視訊結尾。 <p>注意：如果您指定時間不正確，系統會將視訊的第一個時間格用於縮圖。 請參閱<a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>。 </p></p> </td> 
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
