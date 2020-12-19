---
description: 設定使用者的群組成員資格。
seo-description: 設定使用者的群組成員資格。
seo-title: setGroupMembership
solution: Experience Manager
title: setGroupMembership
topic: Scene7 Image Production System API
uuid: 3285fab0-92e4-4b88-9a3c-88cbb97d48c9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 12%

---


# setGroupMembership{#setgroupmembership}

設定使用者的群組成員資格。

語法

## 授權用戶類型{#section-3d6308a8a5694ed085e04d1c37982b9e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-6aeda13b26af4796aad1306ac7a9ad17}

**輸入(setGroupMembershipParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | 否 | 您要設定其群組成員資格的使用者的控制代碼。 |
| ` *`companyHandle`*` | `xsd:string` | 否 | 公司負責人。 |
| ` *`groupHandleArray`*` | `types:HandleArray` | 是 | 用戶所屬的組的句柄陣列。 |

**輸出(setGroupMembershipReturn)**

IPS API不會傳回此作業的回應。

## 範例 {#section-67b86d259df24938896fe19061845811}

此程式碼範例讓使用者成為群組的成員。 使用群組控制代碼陣列將使用者新增至多個群組。

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
