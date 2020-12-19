---
description: PropertySetType和createPropertySetTypeParam欄位的有效值。
seo-description: PropertySetType和createPropertySetTypeParam欄位的有效值。
seo-title: PropertySetType
solution: Experience Manager
title: PropertySetType
topic: Scene7 Image Production System API
uuid: 83220180-3272-4552-974d-a73e6aad3483
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 15%

---


# PropertySetType{#propertysettype}

PropertySetType和createPropertySetTypeParam欄位的有效值。

值包括：

* `UserProperty`
* `CompanyProperty`
* `UserCompanyProperty`

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> typeHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 鍵入handle。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">公司負責人。 <p>注意： 如果公司句柄不存在，則類型為全局。 </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 名稱</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 輸入名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> propertyType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">屬性集類型之一。 請參閱輸入(<span class="codeph"> createPropertySetTypeParam</span>)。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> allowMultiple</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 是否允許將多個屬性集實例附加到此類型的對象。 </td> 
  </tr> 
 </tbody> 
</table>

