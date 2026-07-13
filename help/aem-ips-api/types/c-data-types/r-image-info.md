---
description: 影像資產的屬性。
solution: Experience Manager
title: Imageinfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 058c74b2-634c-49b9-88ab-ab72a030983c
TQID: 'https://experienceleague.adobe.com/EJ-PG1ULUzEvRvHcNDffHoPDT4EJd6fnyPUN50ds9Zk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 150
ht-degree: 3%

---

# [!DNL ImageInfo]{#imageinfo}

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL originalPath]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> <p>原始檔案的相對路徑。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> [!DNL originalFile]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> <p>檔案名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> [!DNL optimizedPath]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> <p>IPS最佳化影像檔案的路徑。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL optimizedFile]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> <p>IPS最佳化的影像檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL maskPath]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> <p>影像遮色片的路徑。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL maskFile]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> <p>遮罩的檔案名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL width]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：int</span> </td> 
   <td colname="col3"> <p>影像寬度（畫素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL height]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：int</span> </td> 
   <td colname="col3"> <p>影像高度（畫素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL fileSize]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：int</span> </td> 
   <td colname="col3"> <p>影像大小，以位元組為單位。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL resolution]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：double</span> </td> 
   <td colname="col3"> <p>每英吋畫素。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL sku]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> <p>產品ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL description]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> <p>影像說明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL comments]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> <p>註解（已棄用）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL userData]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> <p>與影像相關聯的使用者資訊（已棄用）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL anchorX]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：int</span> </td> 
   <td colname="col3"> <p>以畫素為單位的水準錨點。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL anchorY]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：int</span> </td> 
   <td colname="col3"> <p>畫素中的垂直錨點。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL urlModifier]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> <p>影像伺服器URL引數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL urlPostApplyModifier]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> <p>串連到<span class="codeph"> urlModifier</span>結尾的引數。 作為影像伺服器命令的查詢字串格式引數清單。 值位於影像伺服器通訊協定指南中。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL zoomTargets]</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：ZoomTargetArray</span> </td> 
   <td colname="col3"> <p>縮放目標陣列（最多5個）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL masks]</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：MaskArray</span> </td> 
   <td colname="col3"> <p>遮罩陣列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL imageMaps]</span> </span> </td> 
   <td colname="col2"> <span class="codeph">型別：ImageMapsArray</span> </td> 
   <td colname="col3"> <p>影像地圖陣列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

