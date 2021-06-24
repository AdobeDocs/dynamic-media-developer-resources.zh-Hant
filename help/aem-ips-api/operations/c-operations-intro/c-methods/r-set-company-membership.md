---
description: 在一或多個公司中設定使用者的會籍。
solution: Experience Manager
title: setCompanyMembersip
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 43144c75-1d83-4e1d-8319-c3275d349a2f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 14%

---

# setCompanyMembersip{#setcompanymembership}

在一或多個公司中設定使用者的會籍。

語法

## 授權的使用者類型 {#section-0cbcc78cfee64c2baf66f29cce6d0a65}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-3930dc6a016140178631083563598104}

**輸入(setCompanyMembershipParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:sting` | 否 | 用戶句柄。 |
| `*`membershipArray`*` | `types:CompanyMembershipUpdateArray` | 是 | 公司的陣列。 |

**輸出(setCompanyMembershipParam)**

IPS API不會針對此操作傳回回應。

## 範例 {#section-862c0cc32ce0407ab248028e690a8386}

此程式碼範例會新增使用者至公司。 如果需要，請在公司中指定多家公司處理陣列。

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
