---
description: 傳回群組的成員。
solution: Experience Manager
title: getGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 847e4982-219d-47fd-b94c-f7d520ba1367
TQID: 'https://experienceleague.adobe.com/V-LNnM0C56dTOos0qky91nxTLyBJMFxLt4VOD99nTN0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 80
ht-degree: 17%

---

# getGroupMembership{#getgroupmembership}

傳回群組的成員。

語法

## 授權的使用者型別 {#section-35d070e5c4d74ca69df508368953cfb8}

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
| userHandle | `xsd:string` | 否 | 使用者的控制代碼。 |
| companyHandle | `xsd:string` | 否 | 公司的控制代碼。 |

**輸出(getGroupMembershipReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| groupArray | `types:GroupArray` | 是 | 群組陣列。 |

## 範例 {#section-ebb437369f4f4487b3eb2ef0c078b8ae}

此程式碼範例會傳回群組的所有成員。 因為公司和使用者控制代碼是選擇性的，所以操作可以傳回所有群組的所有成員。

**要求**

```java
<ns1:getGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getGroupMembershipParam>
```

**回應**

```java
<getGroupMembershipReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupArray>
      <items>
         <groupHandle>225</groupHandle><companyHandle>47</companyHandle><name>MyGroup</name><isSystemDefined>false</isSystemDefined></items></groupArray></getGroupMembershipReturn>
```
