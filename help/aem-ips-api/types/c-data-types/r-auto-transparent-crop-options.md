---
description: 基於透明度自動裁剪影像時使用的選項。
solution: Experience Manager
title: 自動透明裁剪選項
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 351f63a4-cc1b-4db9-93df-c21acd02e12a
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 12%

---

# [!DNL AutoTransparentCropOptions]{#autotransparentcropoptions}

基於透明度自動裁剪影像時使用的選項。

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
   <td colname="col1"> <span class="codeph"> 容限</span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：雙</span> </td> 
   <td colname="col3">根據透明度從影像邊緣中刪除空白。 使用： 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0以完全匹配顏色。 </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1以啟用最大顏色差異。 </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>
