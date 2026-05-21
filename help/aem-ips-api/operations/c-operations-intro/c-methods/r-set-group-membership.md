---
description: 設定使用者的群組成員資格。
solution: Experience Manager
title: setGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0a355a34-1c2d-48c1-ba12-7d07d1673d09
TQID: 'https://experienceleague.adobe.com/j-wK2g-evSRY0YD3ZspgT--giCkKJl1VBYgPylixVz8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 96
ht-degree: 11%

---

# setGroupMembership{#setgroupmembership}

設定使用者的群組成員資格。

語法

## 授權的使用者型別 {#section-3d6308a8a5694ed085e04d1c37982b9e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-6aeda13b26af4796aad1306ac7a9ad17}

**輸入(setGroupMembershipParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| userHandle | `xsd:string` | 否 | 您要設定其群組成員資格之使用者的控制代碼。 |
| companyHandle | `xsd:string` | 否 | 公司控制代碼。 |
| groupHandleArray | `types:HandleArray` | 是 | 使用者所屬群組的控制代碼陣列。 |

**輸出(setGroupMembershipReturn)**

IPS API未傳回此作業的回應。

## 範例 {#section-67b86d259df24938896fe19061845811}

此程式碼範例將使用者設為群組的成員。 使用群組控制代碼陣列將使用者新增至多個群組。

**要求**

```java
<ns1:setGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>70|kmagnusson@adobe.com</ns1:userHandle>
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray>
      <ns1:items>225</ns1:items>
   </ns1:groupHandleArray>
</ns1:setGroupMembershipParam>
```

**回應**

無。
