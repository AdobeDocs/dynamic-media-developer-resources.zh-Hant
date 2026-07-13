---
description: 將使用者新增至群組陣列。
solution: Experience Manager
title: addGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c5b5e155-d285-4304-98bc-1d938793e2c0
TQID: 'https://experienceleague.adobe.com/E26D4T5xx58eE5G1APbIi46B-SL1BM9YqGibC1n4IVo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 92
ht-degree: 10%

---

# addGroupMembership{#addgroupmembership}

將使用者新增至群組陣列。

語法

## 授權的使用者型別 {#section-fe950150718a474d8df30d0f4453c022}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-e250f6ddb13646808c6a8860b6442bc5}

**輸入(addGroupMembershipParam)**

<table id="table_71AD8902E4854CA5A12379DBA4DF17C7"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname">使用者控制代碼</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>處理您要新增其群組成員資格的使用者。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> groupHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：HandleArray</span> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>您希望公司所屬的群組的控制代碼陣列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**輸出(addGroupMembershipParam)**

IPS API未傳回此作業的回應。

## 範例 {#section-f7a1f40c3d7a40ea964b29056c734d81}

此範例會將群組新增至具有groupHandleArray的公司。 此範例僅使用一個群組。

**要求**

```java {.line-numbers}
<ns1:addGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray><ns1:items>225</ns1:items></ns1:groupHandleArray>
</ns1:addGroupMembershipParam>
```

**回應**

無。

