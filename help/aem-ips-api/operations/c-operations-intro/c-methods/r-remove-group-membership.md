---
description: 從群組陣列中移除使用者。
seo-description: 從群組陣列中移除使用者。
seo-title: removeGroupMembership
solution: Experience Manager
title: removeGroupMembership
topic: Scene7 Image Production System API
uuid: 553d91a3-73d6-4323-9436-a3ba13260a6c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# removeGroupMembership{#removegroupmembership}

從群組陣列中移除使用者。

**刪除命令之間的差異**

* `removeGroupMembers`:從群組移除多個使用者。
* `removeGroupMembership`:從群組陣列中移除個別使用者。

## 授權使用者類型 {#section-83f3048bbe5a4f62b7b14dc9efdd951a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-d6a15fa70d3d4fc69da200cdaf59904e}

**輸入(removeGroupMembershipParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | 否 | 您要移除其群組成員資格的公司的控制代碼。 |
| ` *`groupHandleArray`*` | `types:HandleArray` | 是 | 您希望公司從中移除的群組控制代碼陣列。 |

**輸出(removeGroupMembershipReturn)**

IPS API不會傳回此作業的回應。

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
