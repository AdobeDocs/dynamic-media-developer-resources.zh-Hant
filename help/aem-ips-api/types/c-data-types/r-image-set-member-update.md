---
description: '在此類型中， pageReset欄位對RenderSet和目錄影像資產類型有意義 '
solution: Experience Manager
title: ImageSetMemberUpdate
feature: Dynamic Media Classic, SDK/API，影像集
role: Developer,Administrator
exl-id: 4c598afb-a80c-4fac-997f-ef1c7175430c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 7%

---

# ImageSetMemberUpdate{#imagesetmemberupdate}

在此類型中， pageReset欄位對於RenderSet和目錄影像資產類型有意義：

* 對於`RenderSet`, `pageReset`指示新渲染視圖/色票組的開始。

* 對於目錄，`pageReset`表示新頁面檢視的開始。 每個頁面檢視通常有2個頁面影像，但您可以有更多或更少。

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 影像整合員陣列中的資產句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pageReset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">重設頁面。 <p>忽略設定，且<span class="codeph"> ImageSet</span>和<span class="codeph"> SpinSet</span>的值強制為true。 </p></td> 
  </tr> 
 </tbody> 
</table>
