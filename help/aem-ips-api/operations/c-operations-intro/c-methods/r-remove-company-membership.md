---
description: 從一或多家公司移除使用者。
seo-description: 從一或多家公司移除使用者。
seo-title: removeCompanyMembership
solution: Experience Manager
title: removeCompanyMembership
topic: Scene7 Image Production System API
uuid: af57fde0-2297-41da-87bf-f063fc313264
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# removeCompanyMembership{#removecompanymembership}

從一或多家公司移除使用者。

語法

## 授權使用者類型 {#section-e9a16c8a7d8d4845989a1488c9ca9c98}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-6dfce5e44d8a4799afd0c231a0b10463}

**輸入(removeCompanyMembershipParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | 否 | 包含您要移除之會籍的使用者的控制代碼。 |
| ` *`companyHandleArray`*` | `types:HandleArray` | 是 | 您要移除使用者之公司的控制代碼。 |

**輸出(removeCompanyMembershipReturn)**

IPS API不會傳回此作業的回應。

## 範例 {#section-6b7903195e8647a1bd0502f87387ca62}

此程式碼範例會從公司移除使用者。 省略可選的用戶句柄，以從公司handle陣列中指定的公司中刪除所有用戶。

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
