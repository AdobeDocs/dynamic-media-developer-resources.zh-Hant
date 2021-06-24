---
description: 新增使用者至一或多個公司。
solution: Experience Manager
title: addCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 6efef4fb-f2e5-4c41-b739-a36ac2f17884
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 13%

---

# addCompanyMembership{#addcompanymembership}

新增使用者至一或多個公司。

語法

## 授權的使用者類型 {#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-0e925b91d63e48aa91f0b0014e6a0cab}

**輸入(addCompanyMembershipParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | 否 | 要添加其成員資格的用戶的句柄。 |
| `*`membershipArray`*` | `types:CompanyMembershipUpdateArray` | 是 | 您要新增使用者的公司陣列。 |

**輸出(addCompanyMembershipReturn)**

IPS API不會針對此操作傳回回應。

## 範例 {#section-5469f88bac7047cca131faa6b021e437}

此示例使用`*`companyHandleArray`*`將用戶添加到單個公司。

**請求**

```java
<ns1:addCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      </ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addCompanyMembershipParam>
```

**回答**

無。
