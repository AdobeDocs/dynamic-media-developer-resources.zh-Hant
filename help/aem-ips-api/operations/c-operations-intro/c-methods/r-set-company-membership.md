---
description: 設定使用者在一或多個公司中的成員資格。
solution: Experience Manager
title: setCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 43144c75-1d83-4e1d-8319-c3275d349a2f
TQID: 'https://experienceleague.adobe.com/Nb9XjcAX4NMyne48B9QoVqlhUnhCE5ufIHILopUeAf0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 13%

---

# setCompanyMembership{#setcompanymembership}

設定使用者在一或多個公司中的成員資格。

語法

## 授權的使用者型別 {#section-0cbcc78cfee64c2baf66f29cce6d0a65}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-3930dc6a016140178631083563598104}

**輸入(setCompanyMembershipParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| userHandle | `xsd:sting` | 否 | 使用者控制代碼。 |
| memberlationarray | `types:CompanyMembershipUpdateArray` | 是 | 許多公司。 |

**輸出(setCompanyMembershipParam)**

IPS API未傳回此作業的回應。

## 範例 {#section-862c0cc32ce0407ab248028e690a8386}

此程式碼範例將使用者新增至公司。 如有必要，在公司控制代碼陣列中指定多個公司。

**要求**

```java
<ns1:setCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>3341|juser@scene7.com</ns1:userHandle>
   <ns1:companyHandleArray>
      <ns1:items>137</ns1:items>
   </ns1:companyHandleArray>
</ns1:setCompanyMembershipParam>
```

**回應**

無。

