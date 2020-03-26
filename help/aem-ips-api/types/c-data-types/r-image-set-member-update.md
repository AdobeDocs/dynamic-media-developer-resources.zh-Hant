---
description: '在此類型中，pageReset欄位對RenderSet和Catalog影像資產類型有意義 '
seo-description: '在此類型中，pageReset欄位對RenderSet和Catalog影像資產類型有意義 '
seo-title: ImageSetMemberUpdate
solution: Experience Manager
title: ImageSetMemberUpdate
topic: Scene7 Image Production System API
uuid: b0226d21-87ba-4e07-9819-79c9df3df13c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ImageSetMemberUpdate{#imagesetmemberupdate}

在此類型中，pageReset欄位對RenderSet和Catalog影像資產類型有意義：

* 對於 `RenderSet`, `pageReset` 表示新渲染視圖／色板組的開始。

* 對於目錄， `pageReset` 表示新頁面檢視的開始。 通常每個頁面檢視有2個頁面影像，但您可以擁有更多或更少。

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
   <td colname="col1"> <span class="codeph"> 資 <span class="varname"> 產控制代碼</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 映像整合員陣列中的資產句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pageReset</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">重設頁面。 <p>設定會被忽略，而影像集和回轉集的值 <span class="codeph"> 會強制</span><span class="codeph"> 為true</span>。 </p></td> 
  </tr> 
 </tbody> 
</table>

