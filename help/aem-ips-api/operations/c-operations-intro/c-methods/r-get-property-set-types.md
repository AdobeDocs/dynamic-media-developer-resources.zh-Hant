---
description: 獲取與指定公司關聯的屬性集類型，或者如果未指定公司，則獲取全局屬性集類型。
solution: Experience Manager
title: getPropertySetTypes
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 7686d30b-e071-4950-8af1-4dd25312ce4b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 14%

---

# getPropertySetTypes{#getpropertysettypes}

獲取與指定公司關聯的屬性集類型，或者如果未指定公司，則獲取全局屬性集類型。

語法

## 授權的使用者類型 {#section-9c7c0d2cd2c94dfca3f96774b3a9a2c6}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-ac3ed9e036b54ea993f544046ff0e15d}

**輸入(getPropertySetTypesParam)**

<table id="table_2590368FEEF04AD4B074412CBBA90F88"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名稱 </th> 
   <th colname="col2" class="entry"> 類型 </th> 
   <th colname="col3" class="entry"> 必要 </th> 
   <th colname="col4" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">與屬性集類型關聯的公司的句柄。 <p>如果要返回全局屬性集類型，請忽略。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output(getPropertySetTypesReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`typeArray`*` | `types:PropertySetTypeArray` | 是 | 與指定的公司關聯的屬性集類型的陣列，或者如果未指定公司，則全局屬性集類型。 |

## 範例 {#section-280c406a90864409856aee44d4069a52}

**請求**

```java
<getPropertySetTypesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
  <companyHandle>c|1</companyHandle>
</getPropertySetTypesParam>
```

**回答**

```java
<getPropertySetTypesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
  <typeArray>
    <items>
      <typeHandle>pt|1</typeHandle>
      <companyHandle>c|1</companyHandle>
      <name>SavedSearch</name>
      <propertyType>UserCompanyProperty</propertyType>
      <alllowMultiple>true</alllowMultiple>
    </items>
    <items>
      <typeHandle>pt|2</typeHandle>
      <companyHandle>c|1</companyHandle>
      <name>CompanyMetadata</name>
      <propertyType>CompanyProperty</propertyType>
      <alllowMultiple>true</alllowMultiple>
    </items>
  </typeArray>
</getPropertySetTypesReturn>
```
