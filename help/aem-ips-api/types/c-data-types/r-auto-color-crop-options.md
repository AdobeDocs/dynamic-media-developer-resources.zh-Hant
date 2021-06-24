---
description: 根據顏色自動裁切影像的選項。
solution: Experience Manager
title: AutoColorCropOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 29d3dcfe-fddb-4806-b2aa-b96e9bbcff98
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 13%

---

# AutoColorCropOptions{#autocolorcropoptions}

根據顏色自動裁切影像的選項。

語法

## 參數 {#section-0302e9238dbc4704914e938f42c881e6}

<table id="table_F6A0DBA37F704C2097C617A0A6767566"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名稱 </th> 
   <th colname="col2" class="entry"> 類型 </th> 
   <th colname="col3" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 角</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 選擇自動裁切角。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 容差</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3">顏色匹配規範。 使用： 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0以完全匹配顏色。 </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1以啟用最多的顏色差異。 </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>
