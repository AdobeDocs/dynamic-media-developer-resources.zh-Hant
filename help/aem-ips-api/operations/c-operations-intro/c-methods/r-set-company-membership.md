---
description: 設定一或多家公司的使用者會籍。
solution: Experience Manager
title: setCompanyMembership
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 14%

---


# setCompanyMembership{#setcompanymembership}

設定一或多家公司的使用者會籍。

語法

## 授權用戶類型{#section-0cbcc78cfee64c2baf66f29cce6d0a65}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-3930dc6a016140178631083563598104}

**輸入(setCompanyMembershipParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:sting` | 否 | 使用者控制代碼。 |
| `*`membershArray`*` | `types:CompanyMembershipUpdateArray` | 是 | 眾多公司。 |

**輸出(setCompanyMembershipParam)**

IPS API不會傳回此作業的回應。

## 範例 {#section-862c0cc32ce0407ab248028e690a8386}

此程式碼範例會將使用者新增至公司。 如果需要，在公司處理陣列中指定多家公司。

**請求**

```java
<ns1:setCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>3341|juser@scene7.com</ns1:userHandle>
   <ns1:companyHandleArray>
      <ns1:items>137</ns1:items>
   </ns1:companyHandleArray>
</ns1:setCompanyMembershipParam>
```

**回答**

無。
