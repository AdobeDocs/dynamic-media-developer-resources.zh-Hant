---
description: 新增使用者至一或多家公司。
seo-description: 新增使用者至一或多家公司。
seo-title: addCompanyMembership
solution: Experience Manager
title: addCompanyMembership
topic: Scene7 Image Production System API
uuid: be55041c-fc4e-46e8-bd2c-81b5931406f5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# addCompanyMembership{#addcompanymembership}

新增使用者至一或多家公司。

語法

## 授權使用者類型 {#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-0e925b91d63e48aa91f0b0014e6a0cab}

**輸入(addCompanyMembershipParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | 否 | 您要新增其會籍的使用者的控制代碼。 |
| ` *`membershArray`*` | `types:CompanyMembershipUpdateArray` | 是 | 您要新增使用者的一系列公司。 |

**輸出(addCompanyMembershipReturn)**

IPS API不會傳回此作業的回應。

## 範例 {#section-5469f88bac7047cca131faa6b021e437}

此範例使 ` *`用companyHandleArray`*` ，將使用者新增至單一公司。

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
