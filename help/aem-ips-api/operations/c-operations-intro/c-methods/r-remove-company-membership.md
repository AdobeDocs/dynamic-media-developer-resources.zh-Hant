---
description: 從一個或多個公司中刪除用戶。
solution: Experience Manager
title: removeCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1cb9a286-48a0-4542-a80a-c97fd973474e
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 12%

---

# removeCompanyMembership{#removecompanymembership}

從一個或多個公司中刪除用戶。

語法

## 授權用戶類型 {#section-e9a16c8a7d8d4845989a1488c9ca9c98}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-6dfce5e44d8a4799afd0c231a0b10463}

**輸入(removeCompanyMembershipParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| userHandle | `xsd:string` | 否 | 要刪除的成員資格的用戶的句柄。 |
| companyHandleArray | `types:HandleArray` | 是 | 要從中刪除用戶的公司的句柄。 |

**輸出(removeCompanyMembershipReturn)**

IPS API不會為此操作返迴響應。

## 範例 {#section-6b7903195e8647a1bd0502f87387ca62}

此代碼示例從公司中刪除用戶。 省略可選用戶句柄，以從公司handle陣列中指定的公司中刪除所有用戶。

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
