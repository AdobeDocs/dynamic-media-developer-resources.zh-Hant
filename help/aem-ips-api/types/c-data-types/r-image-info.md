---
description: 影像資產的屬性。
seo-description: 影像資產的屬性。
seo-title: ImageInfo
solution: Experience Manager
title: ImageInfo
topic: Scene7 Image Production System API
uuid: 89138f10-c80b-49b8-886f-45b0960038b8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
   <td colname="col1"> <span class="codeph"> 原 <span class="varname"> 始路徑</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>原始檔案的相對路徑。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> originalFile</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>檔案名稱. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> optimizedPath</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>IPS優化映像檔案的路徑。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 最 <span class="varname"> 佳化檔案</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>IPS最佳化影像檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 遮 <span class="varname"> 色片路徑</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>影像遮色片的路徑。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 遮 <span class="varname"> 色片檔案</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>遮色片的檔案名稱。 </p> </td> 
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
   <td colname="col1"> <span class="codeph"> 檔 <span class="varname"> 案大小</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> <p>影像大小（以位元組為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 解 <span class="varname"> 析度</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3"> <p>每英吋像素數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sku</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>產品 ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 說 <span class="varname"> 明</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>影像描述。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 注釋</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>留言（已過時）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 使 <span class="varname"> 用者資料</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>與影像相關的使用者資訊（已過時）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 錨 <span class="varname"> 點X</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> <p>水準錨點（以像素為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 錨 <span class="varname"> 點Y</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> <p>垂直錨點（以皮克斯為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> url修飾詞</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>影像伺服器URL參數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> urlPostApplyModifier</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>串連至URL修飾詞結尾 <span class="codeph"> 的參數</span>。 對映像伺服器的命令的參數的查詢字串格式清單。 值位於映像伺服器協定指南中。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 縮放 <span class="varname"> 目標</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：ZoomTargetArray</span> </td> 
   <td colname="col3"> <p>縮放目標陣列（最多5個）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 遮 <span class="varname"> 色片</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：MaskArray</span> </td> 
   <td colname="col3"> <p>遮色片陣列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageMaps</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：ImageMapsArray</span> </td> 
   <td colname="col3"> <p>影像地圖陣列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

