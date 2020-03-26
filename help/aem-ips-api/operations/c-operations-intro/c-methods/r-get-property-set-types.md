---
description: 獲取與指定公司關聯的屬性集類型，或者如果未指定公司，則獲取全局屬性集類型。
seo-description: 獲取與指定公司關聯的屬性集類型，或者如果未指定公司，則獲取全局屬性集類型。
seo-title: getPropertySetTypes
solution: Experience Manager
title: getPropertySetTypes
topic: Scene7 Image Production System API
uuid: b707344d-5571-45eb-9e37-cf0894ee81a0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getPropertySetTypes{#getpropertysettypes}

獲取與指定公司關聯的屬性集類型，或者如果未指定公司，則獲取全局屬性集類型。

語法

## 授權使用者類型 {#section-9c7c0d2cd2c94dfca3f96774b3a9a2c6}

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
   <td colname="col1"> <span class="codeph"> 公 <span class="varname"> 司控制</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">屬性集類型與關聯的公司的句柄。 <p>如果要返回全局屬性集類型，則省略。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**輸出(getPropertySetTypesReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`typeArray`*` | `types:PropertySetTypeArray` | 是 | 與指定公司關聯的屬性集類型陣列，或者全域屬性集類型（如果未指定公司）。 |

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

