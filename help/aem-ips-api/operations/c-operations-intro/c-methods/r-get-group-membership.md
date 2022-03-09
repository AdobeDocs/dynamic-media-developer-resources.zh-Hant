---
description: 返回組的成員。
solution: Experience Manager
title: getGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 847e4982-219d-47fd-b94c-f7d520ba1367
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 20%

---

# getGroupMembership{#getgroupmembership}

返回組的成員。

語法

## 授權用戶類型 {#section-35d070e5c4d74ca69df508368953cfb8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-2e92f850254e46e48403acaa215341a5}

**輸入(getGroupMembershipParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| userHandle | `xsd:string` | 否 | 用戶的句柄。 |
| 公司句柄 | `xsd:string` | 否 | 公司的把手。 |

**輸出(getGroupMembershipReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 組陣列 | `types:GroupArray` | 是 | 組陣列。 |

## 範例 {#section-ebb437369f4f4487b3eb2ef0c078b8ae}

此代碼示例返回組的所有成員。 由於公司和用戶句柄是可選的，因此該操作可以返回所有組的所有成員。

**請求**

```java
<ns1:getGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getGroupMembershipParam>
```

**回答**

```java
<getGroupMembershipReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupArray>
      <items>
         <groupHandle>225</groupHandle><companyHandle>47</companyHandle><name>MyGroup</name><isSystemDefined>false</isSystemDefined></items></groupArray></getGroupMembershipReturn>
```
