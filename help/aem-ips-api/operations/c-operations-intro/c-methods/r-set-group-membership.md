---
description: 設定用戶的組成員資格。
solution: Experience Manager
title: setGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 0a355a34-1c2d-48c1-ba12-7d07d1673d09
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 12%

---

# setGroupMembership{#setgroupmembership}

設定用戶的組成員資格。

語法

## 授權的使用者類型 {#section-3d6308a8a5694ed085e04d1c37982b9e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-6aeda13b26af4796aad1306ac7a9ad17}

**輸入(setGroupMembershipParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | 否 | 要設定其組成員資格的用戶的句柄。 |
| `*`companyHandle`*` | `xsd:string` | 否 | 公司負責人。 |
| `*`groupHandleArray`*` | `types:HandleArray` | 是 | 用戶所屬組的句柄陣列。 |

**輸出(setGroupMembershipReturn)**

IPS API不會針對此操作傳回回應。

## 範例 {#section-67b86d259df24938896fe19061845811}

此程式碼範例將使用者成為群組的成員。 使用組句柄陣列向多個組添加用戶。

**請求**

```java
<ns1:setGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>70|kmagnusson@adobe.com</ns1:userHandle>
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray>
      <ns1:items>225</ns1:items>
   </ns1:groupHandleArray>
</ns1:setGroupMembershipParam>
```

**回答**

無。
