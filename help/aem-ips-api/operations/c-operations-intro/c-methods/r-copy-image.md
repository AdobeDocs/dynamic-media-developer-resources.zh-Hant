---
description: 建立現有映像資產的副本。 將應用指定的映像伺服器協定命令來生成新副本
solution: Experience Manager
title: 複製映像
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 059ebbca-2341-444b-850a-1ec9582692ec
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 22%

---

# 複製映像{#copyimage}

建立現有映像資產的副本。 將應用指定的映像伺服器協定命令來生成新副本

語法

## 授權用戶類型 {#section-c9fe7abb550e495f832234f845db7d6e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-bf36fcbfda6742f5b9c6b02ea27e5b9d}

**輸入(copyImageParam)**

<table id="table_F6B14D4875F2424D98B8C4899B1DD867"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> 公司名稱</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>包含映像的公司的句柄。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> 資產句柄</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>影像資源的句柄。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> folderHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>要複製影像的資料夾的句柄。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> 名稱</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>新映像的名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> url修飾符</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**輸出(copyImageParam)**

<table id="table_5E4ED83047314DFABC1BFAAC76C0EAC3"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> 資產句柄</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>複製影像的手柄。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-c30a4017001146e7befbbfc5ffcb7593}

示例代碼複製由公司、資產、資料夾句柄和名稱指定的映像。

**請求**

```java
<copyImageParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|739|1|537</assetHandle>
   <folderHandle>ApiTestCo/</folderHandle>
   <name>Copy_macbookwin1</name>
   <urlModifier/>
</copyImageParam>
```

**回答**

```java
<copyImageReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|943|1|580</assetHandle>
</copyImageReturn>
```
