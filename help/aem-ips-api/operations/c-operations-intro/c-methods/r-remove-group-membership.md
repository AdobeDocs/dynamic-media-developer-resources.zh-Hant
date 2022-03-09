---
description: 從一組組中刪除用戶。
solution: Experience Manager
title: removeGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 892ee01c-e07b-4321-b0b7-5bb606036340
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 10%

---

# removeGroupMembership{#removegroupmembership}

從一組組中刪除用戶。

**刪除命令之間的差異**

* `removeGroupMembers`:從組中刪除多個用戶。
* `removeGroupMembership`:從一組組中刪除單個用戶。

## 授權用戶類型 {#section-83f3048bbe5a4f62b7b14dc9efdd951a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-d6a15fa70d3d4fc69da200cdaf59904e}

**Input(removeGroupMembershipParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| userHandle | `xsd:string` | 否 | 要刪除其組成員資格的公司的句柄。 |
| groupHandleArray | `types:HandleArray` | 是 | 要從中刪除公司的組的句柄陣列。 |

**輸出(removeGroupMembershipReturn)**

IPS API不會為此操作返迴響應。

## 範例 {#section-f8d4181170a243efb9faf5824ae96197}

此代碼示例從組中刪除用戶。

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
