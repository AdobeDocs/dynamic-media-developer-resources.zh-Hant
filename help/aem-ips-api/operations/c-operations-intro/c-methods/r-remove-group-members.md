---
description: 從特定群組移除公司使用者。
solution: Experience Manager
title: removeGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 8a9b7d54-d11b-41a8-9783-573a316e0ac6
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 9%

---

# removeGroupMembers{#removegroupmembers}

從特定群組移除公司使用者。

**刪除命令之間的差異**

* `removeGroupMembers`:從群組中移除多個使用者。
* `removeGroupMembership`:從群組陣列中移除個別使用者。

## 授權的使用者類型 {#section-2c64cdac15184fbba6c7b2945b5d87f7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-b5596614a3be4ce5962455884e4636af}

**輸入(removeGroupMembersParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司的控制代碼，以及您要與之合作的使用者。 |
| `*`groupHandle`*` | `xsd:string` | 是 | 組句柄。 |
| `*`userHandleArray`*` | `types:HandleArray` | 是 | 要刪除其組成員資格的用戶的句柄陣列。 |

**輸出(removeGroupMembersParam)**

IPS API不會針對此操作傳回回應。

## 範例 {#section-9eedac852cea46ec80de6a6928bf97ac}

此程式碼範例會從指定的公司移除使用者。 使用用戶句柄陣列從組中刪除多個用戶。

**請求**

```java
<ns1:removeGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
   <ns1:userHandleArray>
      <ns1:items>621|jduvar@adobe.com</ns1:items>
   </ns1:userHandleArray>
</ns1:removeGroupMembersParam>
```

**回答**

無。
