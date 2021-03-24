---
description: '在此類型中，pageReset欄位對RenderSet和Catalog影像資產類型有意義 '
solution: Experience Manager
title: ImageSetMemberUpdate
feature: Dynamic Media經典，SDK/API，影像集
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 7%

---


# ImageSetMemberUpdate{#imagesetmemberupdate}

在此類型中，pageReset欄位對RenderSet和Catalog影像資產類型有意義：

* 對於`RenderSet`, `pageReset`表示新渲染視圖／色票組的開始。

* 對於目錄，`pageReset`表示新頁面視圖的開始。 通常每個頁面檢視有2個頁面影像，但您可以擁有更多或更少。

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
   <td colname="col3"> 映像整合員陣列中的資產句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pageReset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">重設頁面。 <p>設定被忽略，並且<span class="codeph"> ImageSet</span>和<span class="codeph"> SpinSet</span>的值強制為true。 </p></td> 
  </tr> 
 </tbody> 
</table>

