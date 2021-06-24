---
description: 從群組陣列中移除使用者。
solution: Experience Manager
title: removeGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 892ee01c-e07b-4321-b0b7-5bb606036340
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 10%

---

# removeGroupMembership{#removegroupmembership}

從群組陣列中移除使用者。

**刪除命令之間的差異**

* `removeGroupMembers`:從群組中移除多個使用者。
* `removeGroupMembership`:從群組陣列中移除個別使用者。

## 授權的使用者類型 {#section-83f3048bbe5a4f62b7b14dc9efdd951a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-d6a15fa70d3d4fc69da200cdaf59904e}

**輸入(removeGroupMembershipParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | 否 | 您要移除其群組成員資格之公司的控制代碼。 |
| `*`groupHandleArray`*` | `types:HandleArray` | 是 | 要從中刪除公司的組的句柄陣列。 |

**輸出(removeGroupMembershipReturn)**

IPS API不會針對此操作傳回回應。

## 範例 {#section-f8d4181170a243efb9faf5824ae96197}

此程式碼範例會從群組中移除使用者。

**請求**

```java
<ns1:removeGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>47</ns1:userHandle>
   <ns1:groupHandleArray>
      <ns1:items>225</ns1:items>
   </ns1:groupHandleArray>
</ns1:removeGroupMembershipParam>
```

**回答**

無。
