---
description: 從特定群組移除公司使用者。
seo-description: 從特定群組移除公司使用者。
seo-title: removeGroupMembers
solution: Experience Manager
title: removeGroupMembers
topic: Scene7 Image Production System API
uuid: dd0ea335-bbd0-43b1-830b-77f32dc39b12
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# removeGroupMembers{#removegroupmembers}

從特定群組移除公司使用者。

**刪除命令之間的差異**

* `removeGroupMembers`:從群組移除多個使用者。
* `removeGroupMembership`:從群組陣列中移除個別使用者。

## 授權使用者類型 {#section-2c64cdac15184fbba6c7b2945b5d87f7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-b5596614a3be4ce5962455884e4636af}

**輸入(removeGroupMembersParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 與您要搭配使用之使用者的公司控制代碼。 |
| ` *`groupHandle`*` | `xsd:string` | 是 | 群組控制代碼。 |
| ` *`userHandleArray`*` | `types:HandleArray` | 是 | 您要移除其群組成員資格的使用者的控制代碼陣列。 |

**輸出(removeGroupMembersParam)**

IPS API不會傳回此作業的回應。

## 範例 {#section-9eedac852cea46ec80de6a6928bf97ac}

此程式碼範例會從指定的公司移除使用者。 使用使用者控制代碼陣列，從群組移除多個使用者。

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
