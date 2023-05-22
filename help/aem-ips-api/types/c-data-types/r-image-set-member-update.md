---
description: 在此類型中，pageReset欄位對RenderSet和Catalog映像資產類型有意義
solution: Experience Manager
title: ImageSetMemberUpdate
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 4c598afb-a80c-4fac-997f-ef1c7175430c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 7%

---

# [!DNL ImageSetMemberUpdate]{#imagesetmemberupdate}

在此類型中，pageReset欄位對RenderSet和Catalog映像資產類型有意義：

* 對於 `RenderSet`。 `pageReset` 指示新渲染視圖/色板組的開始。

* 對於目錄， `pageReset` 指示新頁面視圖的開始。 通常，每個頁面視圖有2個頁面影像，但可以有更多或更少。

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> 資產句柄</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 映像整合員陣列中的資產句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 頁面重置</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">重置頁面。 <p>設定被忽略，值被強制為true <span class="codeph"> 影像集</span> 和 <span class="codeph"> 旋轉集</span>。 </p></td> 
  </tr> 
 </tbody> 
</table>
