---
description: 取得公司陣列中的使用者會籍。
solution: Experience Manager
title: getCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 17%

---


# getCompanyMembership{#getcompanymembership}

取得公司陣列中的使用者會籍。

語法

## 授權用戶類型{#section-f8bba547e1f648648be99dc48fd72b5d}

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
| `*`membershArray`*` | `types:CompanyMembershipArray` | 是 | 公司會籍的陣列。 |

## 範例 {#section-e4958d104ea344a4a79f57d07b46eba7}

此程式碼範例會取用使用者控制代碼，並取得陣列中所有使用者的公司會籍。 回應已因簡短而截斷。

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

