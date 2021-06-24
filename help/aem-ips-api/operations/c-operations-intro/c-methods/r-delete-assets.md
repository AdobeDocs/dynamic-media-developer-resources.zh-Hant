---
description: 刪除多個資產。
solution: Experience Manager
title: deleteAssets
feature: Dynamic Media Classic,SDK/API，資產管理
role: Developer,Administrator
exl-id: 487f83e6-f713-40e9-a442-e1179b30012c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 15%

---

# deleteAssets{#deleteassets}

刪除多個資產。

語法

## 授權用戶類型 {#section-a6bc555b8ac840c98835b73fbf838d70}

* `IpsUser`
* `IspAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-4dc888e77d974ac794b553616dd11e86}

**輸入(deleteAssetsParam)**

<table id="table_AAA6845769DB4B129C8A660D0CBA348A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名稱 </p> </th> 
   <th colname="col2" class="entry"> <p>類型 </p> </th> 
   <th colname="col3" class="entry"> <p>必要 </p> </th> 
   <th colname="col4" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>資產所屬公司的控制代碼。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：HandleArray</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>要刪除的資產陣列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**輸出(deleteAssetsParam)**

<table id="table_0C6D8D51A79248ACA2022DBB754A9B9C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名稱 </p> </th> 
   <th colname="col2" class="entry"> <p>類型 </p> </th> 
   <th colname="col3" class="entry"> <p>必要 </p> </th> 
   <th colname="col4" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> successCount</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>成功刪除的資產數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> warningCount</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>操作嘗試刪除時產生警告的資產。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> errorCount</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>操作嘗試刪除時產生錯誤的資產。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> warningDetailArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：AssetOperationFaultArray</span> </p> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>與資產相關聯的詳細資訊陣列，當操作嘗試刪除資產時產生警告。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> errorDetailArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：AssetOperationFaultArray</span> </p> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>與資產相關聯的詳細資訊陣列，當操作嘗試刪除資產時產生錯誤。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-aaad1933bf86479eb6cb476cec7d4587}

此程式碼範例會將控制代碼傳送至公司，並將`deleteAssetsParam`請求中的資產控制代碼陣列傳送至網站服務伺服器。 `deleteAssetsReturn` 傳回成功計數2，表示兩個資產皆已刪除。

**請求**

```java
<deleteAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</deleteAssetsParam>
```

**回答**

```java
<deleteAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</deleteAssetsReturn>
```
