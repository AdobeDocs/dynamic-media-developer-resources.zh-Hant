---
description: 在此型別中， pageReset欄位對RenderSet和目錄影像資產型別有意義
solution: Experience Manager
title: ImageSetMemberupdate
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 4c598afb-a80c-4fac-997f-ef1c7175430c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 3%

---

# [!DNL ImageSetMemberUpdate]{#imagesetmemberupdate}

在此型別中， pageReset欄位對RenderSet和目錄影像資產型別有意義：

* 對於`RenderSet`，`pageReset`表示新轉譯器檢視/色票群組的開始。

* 對於目錄，`pageReset`表示新頁面檢視的開始。 一般而言，每個頁面檢視有2個頁面影像，但您可以有更多的或較少的頁面檢視。

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
   <td colname="col1"> <span class="codeph"> <span class="varname">資產控制代碼</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 影像整合員陣列中的資產控制代碼。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pageReset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：布林值</span> </td> 
   <td colname="col3">重設頁面。 <p>已略過設定，且已強制將<span class="codeph">影像集</span>和<span class="codeph">迴轉集</span>的值設為true。 </p></td> 
  </tr> 
 </tbody> 
</table>
