---
description: 一種可選類型，允許您選擇特定視頻幀作為縮略圖。
solution: Experience Manager
title: 縮略圖選項
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7d84590d-2227-4d9a-9cb0-0f4b1fcabd8e
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 6%

---

# [!DNL ThumbnailOptions]{#thumbnailoptions}

一種可選類型，允許您選擇特定視頻幀作為縮略圖。

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> 縮略圖時間</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> <p>為要用於視頻縮略圖的幀設定時間（從視頻啟動開始以毫秒為單位）。 值範圍從0到視頻結尾。 <p>注：如果您未正確指定時間，則系統會將視頻的第一幀用於縮略圖。 請參閱 <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> 媒體選項</a>。 </p></p> </td> 
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
