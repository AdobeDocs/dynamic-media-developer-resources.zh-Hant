---
description: 新增使用者至一或多家公司。
solution: Experience Manager
title: addCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 13%

---


# addCompanyMembership{#addcompanymembership}

新增使用者至一或多家公司。

語法

## 授權用戶類型{#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-0e925b91d63e48aa91f0b0014e6a0cab}

**輸入(addCompanyMembershipParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | 否 | 您要新增其會籍的使用者的控制代碼。 |
| `*`membershArray`*` | `types:CompanyMembershipUpdateArray` | 是 | 您要新增使用者的一系列公司。 |

**輸出(addCompanyMembershipReturn)**

IPS API不會傳回此作業的回應。

## 範例 {#section-5469f88bac7047cca131faa6b021e437}

此範例使用`*`companyHandleArray`*`將使用者新增至單一公司。

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
