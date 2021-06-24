---
description: 在公司陣列中取得使用者的會籍。
solution: Experience Manager
title: getCompanyMembersing
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 53af8a97-208c-4c44-93d6-aa36a459af51
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 17%

---

# getCompanyMembersing{#getcompanymembership}

在公司陣列中取得使用者的會籍。

語法

## 授權的使用者類型 {#section-f8bba547e1f648648be99dc48fd72b5d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-8745c360c3e1400a88e9bdb26bcb93de}

**輸入(getCompanyMembershipParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | 否 | 要獲取其成員資格的用戶的句柄。 |

**輸出(getCompanyMembershipReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`membershipArray`*` | `types:CompanyMembershipArray` | 是 | 公司會籍陣列。 |

## 範例 {#section-e4958d104ea344a4a79f57d07b46eba7}

此程式碼範例取用使用者控制代碼，並取得陣列中所有使用者的公司會籍。 回應已為簡潔而截斷。

**請求**

```java
<ns1:getCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>70|kmagnusson@adobe.com</ns1:userHandle>
</ns1:getCompanyMembershipParam>
```

**回答**

```java
<getCompanyMembershipReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <membershipArray>
      <items>
         <companyHandle>48</companyHandle>
         <name>AIR</name>
         <rootPath>AIR/</rootPath>
         <expires>2101-01-31T23:00:00.485-08:00</expires>
      </items>
      ...
    </membershipArray>
</getCompanyMembershipReturn>
```
