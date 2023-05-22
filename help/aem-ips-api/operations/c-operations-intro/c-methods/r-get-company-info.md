---
description: 返回有關指定公司的資訊，包括公司句柄、公司名稱、根路徑和到期日期。 必須指定要檢索其資訊的companyHandle或companyName。
solution: Experience Manager
title: getCompanyInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 72bd223b-c99a-48a3-9c0a-d1af392d904c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 10%

---

# getCompanyInfo{#getcompanyinfo}

返回有關指定公司的資訊，包括公司句柄、公司名稱、根路徑和到期日期。 必須指定要檢索其資訊的companyHandle或companyName。

語法

## 授權用戶類型 {#section-74f20fb8602e4f96810795bc4b6f7fdf}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-7dec8871c89a414c9f066adade1831d8}

**輸入(getCompanyInfoParam)**

<table id="table_DD2688C9DA9F49C9ABCA24944829B3E5"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> 公司句柄</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>要麼 <span class="codeph"> <span class="varname"> 公司句柄</span> </span> 或 <span class="codeph"> <span class="varname"> 公司名稱</span> </span> 。 </p> </td> 
   <td colname="col4"> <p>您要獲取其資訊的公司的句柄。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> 公司名稱</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>要麼 <span class="codeph"> <span class="varname"> 公司句柄</span> </span> 或 <span class="codeph"> <span class="varname"> 公司名稱</span> </span> 。 </p> </td> 
   <td colname="col4"> <p>您要獲取其資訊的公司的名稱。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**輸出(getCompanyInfoReturn)**

<table id="table_634D4E274BA7494C9C917FD244286F0D"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> 公司資訊</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：公司</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>處理和有關公司的其他說明性資訊。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-3d5342aa7cb34b1fa84d7dea6e16e4aa}

此代碼示例使用公司名稱和句柄返回有關公司的所有資訊。 它返回與建立公司時收到的響應類似的資料。

**請求**

```java
<ns1:getCompanyInfoParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyName>Planetary</ns1:companyName>
</ns1:getCompanyInfoParam>
```

**回答**

```java
<ns1:getCompanyInfoReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyInfo>
      <ns1:companyHandle>137</ns1:companyHandle>
      <ns1:name>Planetary</ns1:name>
      <ns1:rootPath>Planetary/</ns1:rootPath>
      <ns1:expires>2101-01-31T23:00:00.030Z</ns1:expires>
   </ns1:companyInfo>
</ns1:getCompanyInfoReturn>
```
