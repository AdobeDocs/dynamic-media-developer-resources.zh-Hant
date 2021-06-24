---
description: 從一或多個公司移除使用者。
solution: Experience Manager
title: removeCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 1cb9a286-48a0-4542-a80a-c97fd973474e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 11%

---

# removeCompanyMembership{#removecompanymembership}

從一或多個公司移除使用者。

語法

## 授權的使用者類型 {#section-e9a16c8a7d8d4845989a1488c9ca9c98}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-6dfce5e44d8a4799afd0c231a0b10463}

**輸入(removeCompanyMembershipParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | 否 | 具有要刪除的成員資格的用戶的句柄。 |
| `*`companyHandleArray`*` | `types:HandleArray` | 是 | 您要移除使用者之公司的控制代碼。 |

**輸出(removeCompanyMembershipReturn)**

IPS API不會針對此操作傳回回應。

## 範例 {#section-6b7903195e8647a1bd0502f87387ca62}

此程式碼範例會從公司中移除使用者。 忽略可選用戶句柄，從公司句柄陣列中指定的公司中刪除所有用戶。

**請求**

```java
<ns1:removeCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:removeCompanyMembershipParam>
```

**回答**

無。
