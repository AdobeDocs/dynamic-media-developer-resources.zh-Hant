---
description: 更新欄位中繼資料。
solution: Experience Manager
title: updateMetadataField
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 67506e76-aa23-46a7-a900-03d89b4266fd
TQID: 'https://experienceleague.adobe.com/KWv2pWCAN3eKZ5FLG2e62qGKSLpMt0eH5QBbQpSOTNM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 147
ht-degree: 12%

---

# updateMetadataField{#updatemetadatafield}

更新欄位中繼資料。

語法

## 授權的使用者型別 {#section-540e91823fee49a4920ca738f7bfeb99}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-69681ed1ddff437ca1c73f46fe835c96}

**輸入(updateMetadataFieldParam)**

<table id="table_65D6EE6C402E4F01819822A855B6BB7F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 引數名稱 </th> 
   <th colname="col2" class="entry"> 類型 </th> 
   <th colname="col3" class="entry"> 必要 </th> 
   <th colname="col4" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 公司控制代碼。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 中繼資料欄位控制代碼。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">名稱</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 中繼資料欄位名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 中繼資料欄位值。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isHidden</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：布林值</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 隱藏或公開IPS系統特定的中繼資料。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname">已強制</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd：布林值</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>布林值標幟，指出在設定值時，是否強制執行（驗證）中繼資料欄位。 </p> <p>若設為true，則若在<span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>中設定了不合法的值，則會擲回錯誤。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 可讓您建立一組選取標籤可指向的共用列舉值。 </td> 
  </tr> 
 </tbody> 
</table>

**輸出(updateMetadataFieldReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| fieldHandle | `xsd:string` | 是 | 中繼資料欄位控制代碼。 |

## 範例 {#section-bb7d93ab6d914ddfa294e08983e589ee}

此程式碼範例更新會將新名稱和預設值指派給中繼資料欄位。 回應會將控制代碼傳回至更新的欄位。

**要求**

```java
<updateMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <fieldHandle>m|21|IMAGE|createMetadataField</fieldHandle>
   <name>updateMetadataField</name>
   <defaultValue>Default</defaultValue>
</updateMetadataFieldParam>
```

**回應**

```java
<updateMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <fieldHandle>m|21|IMAGE|updateMetadataField</fieldHandle>
</updateMetadataFieldReturn>
```

