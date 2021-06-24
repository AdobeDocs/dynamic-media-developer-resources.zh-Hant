---
description: 設定屬於特定公司之使用者的群組成員資格。
solution: Experience Manager
title: setGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 81348da7-6733-4da9-8a0a-376fccf791ea
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 9%

---

# setGroupMembers{#setgroupmembers}

設定屬於特定公司之使用者的群組成員資格。

如果您沒有完成此操作的權限，則操作會擲回驗證錯誤。 如果使用者控制代碼陣列中的任何使用者不屬於公司控制代碼中指定的公司，則也會採用此方法。

## 授權的使用者類型 {#section-4523594039c24aa29c8d0d5c9c415391}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-6a18562fc8e942af94be10bbb8c51151}

**輸入(setGroupMembersParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司負責人。 |
| `*`groupHandle`*` | `xsd:string` | 是 | 組句柄。 |
| `*`userHandleArray`*` | `types:HandleArray` | 是 | 要設定其組成員資格的用戶的句柄陣列。 |

**輸出(setGroupMembersReturn)**

IPS API不會針對此操作傳回回應。

## 範例 {#section-9c528c3f44a141ce9eaddf634f26c487}

此程式碼範例會設定單一使用者的群組成員資格。

**請求**

```java
<ns1:setGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
   <ns1:userHandleArray>
      <ns1:items>70|kmagnusson@adobe.com</ns1:items>
   </ns1:userHandleArray>
</ns1:setGroupMembersParam>
```

**回答**

無。
