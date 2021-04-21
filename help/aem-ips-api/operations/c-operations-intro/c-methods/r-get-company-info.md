---
description: 傳回指定公司的相關資訊，包括公司控制代碼、公司名稱、根路徑和到期日。 您必須指定要擷取其資訊的companyHandle或companyName。
solution: Experience Manager
title: getCompanyInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 10%

---


# getCompanyInfo{#getcompanyinfo}

傳回指定公司的相關資訊，包括公司控制代碼、公司名稱、根路徑和到期日。 您必須指定要擷取其資訊的companyHandle或companyName。

語法

## 授權用戶類型{#section-74f20fb8602e4f96810795bc4b6f7fdf}

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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>需要<span class="codeph"> <span class="varname"> companyHandle</span> </span>或<span class="codeph"> <span class="varname"> companyName</span> </span>。 </p> </td> 
   <td colname="col4"> <p>您要取得其資訊之公司的控制代碼。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyName</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>需要<span class="codeph"> <span class="varname"> companyHandle</span> </span>或<span class="codeph"> <span class="varname"> companyName</span> </span>。 </p> </td> 
   <td colname="col4"> <p>您要取得其資訊的公司名稱。 </p> </td> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyInfo</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：公司</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>處理和其他有關公司的描述性資訊。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-3d5342aa7cb34b1fa84d7dea6e16e4aa}

此程式碼範例會使用公司名稱和控制代碼，傳回有關公司的所有資訊。 它會傳回類似於建立公司時所收到回應的資料。

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

