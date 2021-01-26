---
description: 獨立移動多個資產。 它使用assetMoveArray中包含的AssetMove類型來實現此目的。 每個AssetMove欄位都包含一個目標資料夾。
seo-description: 獨立移動多個資產。 它使用assetMoveArray中包含的AssetMove類型來實現此目的。 每個AssetMove欄位都包含一個目標資料夾。
seo-title: moveAssets
solution: Experience Manager
title: moveAssets
topic: Dynamic Media Image Production System API
uuid: 178f9979-fff5-45ce-a001-1263d1770ea8
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 11%

---


# moveAssets{#moveassets}

獨立移動多個資產。 它使用assetMoveArray中包含的AssetMove類型來實現此目的。 每個AssetMove欄位都包含一個目標資料夾。

語法

## 授權用戶類型{#section-4166515fd9d8487b8af37465ce61802b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-7d47f663474b41cc83439288ac133cc5}

**輸入(moveAssetsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 資產要移動的公司的控制代碼。 |
| `*`assetMoveArray`*` | `types:AssetMoveArray` | 是 | 資產移動陣列。 它包含資產和資產目標資料夾。 |

**輸出(moveAssetsReturn)**

<table id="table_FD902FAB4F98413C8A051270ADD7D9C7"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> successCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 已成功移動資產計數。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 當操作嘗試移動時產生警告的資產計數。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 當操作嘗試移動錯誤時產生錯誤的資產計數。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningDetailArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：AssetOperationFaultArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <span class="codeph"> AssetOperationFaults，其中包含：</span> 
    <ul id="ul_689F4A87A68140F18DFB43868226A409"> 
     <li id="li_274C8BF5932F4AF584AA92F25E0F33C6">拋出警告的資產。 </li> 
     <li id="li_5CC4A9120CA94F968CAF0D0135C49E0A">警告代碼。 </li> 
     <li id="li_AEC91FA68B2E43BC8BAA108C743F5667">警告的原因。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorDetailArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：AssetOperationFaultArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <span class="codeph"> AssetOperationFaults，其中包含：</span> 
    <ul id="ul_C397BC384A134F429D01ADA28DF2E097"> 
     <li id="li_EAEBB5F539164480BA9EAA7C8FFBF69A">擲回錯誤的資產。 </li> 
     <li id="li_F96D5FBB2F7A402AA36D8DFA3971391D">錯誤代碼。 </li> 
     <li id="li_F610415E416F43DDA4B1DBF1897E2F61">錯誤的原因。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-c31ed4c004ab4b3fa42c96d26ceb5ce7}

此程式碼範例會將資產移至`assetMoveArray`所指定的特定位置。 陣列包括資產控制代碼及其資料夾控制代碼。 回應指出資產已成功移動。

**請求**

```java
<moveAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetMoveArray>
      <items>
          <assetHandle>a|942|1|579</assetHandle>
          <folderHandle>ApiTestCo/uploads/</folderHandle>
      </items>
      <items>
         <assetHandle>a|943|1|580</assetHandle>
         <folderHandle>ApiTestCo/uploads/</folderHandle>
      </items>
   </assetMoveArray>
</moveAssetsParam>
```

**回答**

```java
<moveAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</moveAssetsReturn>
```

