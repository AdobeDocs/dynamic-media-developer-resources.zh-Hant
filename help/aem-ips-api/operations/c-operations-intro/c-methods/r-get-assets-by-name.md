---
description: 根據資產名稱陣列傳回資產。
seo-description: 根據資產名稱陣列傳回資產。
seo-title: getAssetsByName
solution: Experience Manager
title: getAssetsByName
topic: Scene7 Image Production System API
uuid: e86b3b16-ad93-4f70-9f59-b72395513c4c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getAssetsByName{#getassetsbyname}

根據資產名稱陣列傳回資產。

語法

## 授權使用者類型 {#section-754790841ea242d5ae8bedd587d7730e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>僅傳回使用者具有讀取存取權的資產。

## 參數 {#section-f64e93c127b84a29aa3bf2fdd916cca9}

**輸入(getAssetsByNameParam)**

<table id="table_CE7B503B0E074719A523B458DF3A7286"> 
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
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 公司的把手。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessUserHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 以其他使用者身分提供存取權。 僅供管理員使用。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessGroupHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 用於依特定群組篩選。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nameArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：StringArray</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 要擷取的資產名稱陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 已擷取資產允許的資產類型陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 已檢索資產排除的資產類型陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 已擷取資產允許的資產子類型陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> strictSubTypeCheck</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>如果 <span class="codeph"> true</span><span class="codeph"> 和assetSubTypeArray不是空的，則只會傳回子類型位於</span><span class="codeph"></span> assetSubTypeArray中的資產。 </p> <p>若為 <span class="codeph"> false</span>，則會包含未定義子類型的資產。 </p> <p>The default value is <span class="codeph"> false</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> responseFieldArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 包含回應中包含的欄位和子欄位清單。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> excludeFieldArray <span class="varname"> (排除欄位陣列</span> ) </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 包含從回應中排除的欄位和子欄位清單。 </td> 
  </tr> 
 </tbody> 
</table>

**輸出(getAssetsByNameReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`assetArray`*` | `types:AssetArray` | 否 | 符合篩選條件的資產陣列。 |

## 範例 {#section-3b7447398e574c88aeaf8ca159cc78dd}

此程式碼範例會傳回兩個影像類型資產。

**請求**

```java
<getAssetsByNameParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <nameArray>
      <items>B010</items>
      <items>IMG_0103</items>
   </nameArray>
   <assetTypeArray>
      <items>Image</items>
   </assetTypeArray>
</getAssetsByNameParam>
```

**回答**

```java
<getAssetsByNameReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <assetArray>
      <items>
         <assetHandle>a|210</assetHandle>
         <type>Image</type>
         <name>B010</name>
         ...</items>
      <items>
         <assetHandle>a|189</assetHandle>
         <type>Image</type>
         <name>IMG_0103</name>
         ...
      </items>
   </assetArray>
</getAssetsByNameReturn>
```

