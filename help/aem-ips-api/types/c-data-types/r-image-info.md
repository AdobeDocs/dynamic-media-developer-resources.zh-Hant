---
description: 影像資產的屬性。
solution: Experience Manager
title: ImageInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 058c74b2-634c-49b9-88ab-ab72a030983c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 23%

---

# ImageInfo{#imageinfo}

影像資產的屬性。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名稱 </p> </th> 
   <th colname="col2" class="entry"> <p>類型 </p> </th> 
   <th colname="col3" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> originalPath</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>原始檔案的相對路徑。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> originalFile</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>檔案名稱. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> optimizedPath</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>IPS優化映像檔案的路徑。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizedFile</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>IPS優化的映像檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> maskPath</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>影像遮色片的路徑。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> maskFile</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>遮色片的檔案名。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> width</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> <p>影像寬度（像素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> height</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> <p>影像高度（像素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fileSize</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> <p>影像大小（以位元組為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 解析度</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3"> <p>每英吋像素。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sku</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>產品 ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 說明</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>影像說明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 評論</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>留言（已廢止）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> userData</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>與影像相關聯的使用者資訊（已淘汰）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> anchorX</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> <p>水準錨點（像素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> anchorY</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> <p>垂直錨點。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> urlModifier</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>影像伺服器URL參數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> urlPostApplyModifier</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>串連至<span class="codeph"> urlModifier</span>結尾的參數。 對影像伺服器的命令的參數的查詢字串格式清單。 值在映像伺服器協定指南中。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> zoomTargets</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：ZoomTargetArray</span> </td> 
   <td colname="col3"> <p>縮放目標的陣列（最多5個）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 遮罩</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：MaskArray</span> </td> 
   <td colname="col3"> <p>掩碼陣列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageMaps</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：ImageMapsArray</span> </td> 
   <td colname="col3"> <p>影像映射陣列。 </p> </td> 
  </tr> 
 </tbody> 
</table>
