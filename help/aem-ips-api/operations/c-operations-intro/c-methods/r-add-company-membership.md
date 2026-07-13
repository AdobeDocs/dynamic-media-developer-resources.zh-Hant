---
description: 新增使用者至一或多個公司。
solution: Experience Manager
title: addCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6efef4fb-f2e5-4c41-b739-a36ac2f17884
TQID: 'https://experienceleague.adobe.com/VNnc-lxt0VHsrYBfJHUVTfK7Hqb42u-P-DtxNdQvS8o'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 83
ht-degree: 12%

---

# addCompanyMembership{#addcompanymembership}

新增使用者至一或多個公司。

語法

## 授權的使用者型別 {#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-0e925b91d63e48aa91f0b0014e6a0cab}

**輸入(addCompanyMembershipParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| userHandle | `xsd:string` | 否 | 您要新增其成員資格之使用者的控制代碼。 |
| memberlationarray | `types:CompanyMembershipUpdateArray` | 是 | 您要新增使用者的公司陣列。 |

**輸出(addCompanyMembershipReturn)**

IPS API未傳回此作業的回應。

## 範例 {#section-5469f88bac7047cca131faa6b021e437}

此範例使用companyHandleArray將使用者新增至單一公司。

**要求**

```javascript {.line-numbers}
<ns1:addCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      </ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addCompanyMembershipParam>
```

**回應**

無。

