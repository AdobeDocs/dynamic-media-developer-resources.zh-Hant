---
description: 建立或編輯中繼資料欄位。 忽略可選欄位句柄以建立新元資料欄位。
solution: Experience Manager
title: saveMetadataField
feature: Dynamic Media Classic,SDK/API，中繼資料
role: Developer,Administrator
exl-id: 56a45324-5027-4375-a790-c965f682e4b9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 16%

---

# saveMetadataField{#savemetadatafield}

建立或編輯中繼資料欄位。 忽略可選欄位句柄以建立新元資料欄位。

>[!NOTE]
>
>此方法已淘汰。

## 授權的使用者類型 {#section-0c1cbde0863346f8a31b32fd06ab2926}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-ec6827d485a143f4a059a92b18e40f4e}

**輸入(saveMetadataFieldParam)**

<table id="table_C944A44352F2475A89CE86F3DB1B648A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 參數名稱 </th> 
   <th colname="col2" class="entry"> 類型 </th> 
   <th colname="col3" class="entry"> 必要 </th> 
   <th colname="col4" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 公司的把手。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 欄位句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 選擇要儲存中繼資料的資產類型。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 名稱</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 欄位名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 選擇中繼資料欄位類型。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 所有資產欄位的預設值。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isHidden</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 隱藏或公開IPS系統特定元資料。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnforced</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>布林值標幟，指出設定值時是否強制（驗證）中繼資料欄位。 </p> <p>如果設為true，則如果在<span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>中設定了非法值，則會擲回錯誤。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**輸出(saveMetadataFieldReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`fieldHandle`*` | `xsd:string` | 是 | 新中繼資料欄位的處理。 |

## 範例 {#section-4441c26d1f41466ba972b43dd5189e89}

此程式碼範例會建立受資產類型和中繼資料欄位類型字串常數限制的新中繼資料欄位。 如果`fieldHandle`元素具有有效的欄位句柄值，它將更改元資料值，並獲取您在請求中指定的相同欄位句柄。

**請求**

```java
<ns1:saveMetadataFieldParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetType>Pdf</ns1:assetType>
   <ns1:name>Resolution</ns1:name>
   <ns1:fieldType>String</ns1:fieldType>
   <ns1:defaultValue>120</ns1:defaultValue>
</ns1:saveMetadataFieldParam>
```

**回答**

```java
<saveMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <fieldHandle>47|ALL|Resolution</fieldHandle>
</saveMetadataFieldReturn>
```
