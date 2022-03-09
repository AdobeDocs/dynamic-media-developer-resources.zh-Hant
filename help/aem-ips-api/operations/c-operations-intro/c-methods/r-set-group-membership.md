---
description: 為用戶設定組成員身份。
solution: Experience Manager
title: setGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0a355a34-1c2d-48c1-ba12-7d07d1673d09
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 13%

---

# setGroupMembership{#setgroupmembership}

為用戶設定組成員身份。

語法

## 授權用戶類型 {#section-3d6308a8a5694ed085e04d1c37982b9e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-6aeda13b26af4796aad1306ac7a9ad17}

**Input(setGroupMembershipParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| userHandle | `xsd:string` | 否 | 要設定其組成員資格的用戶的句柄。 |
| 公司句柄 | `xsd:string` | 否 | 公司負責。 |
| groupHandleArray | `types:HandleArray` | 是 | 用戶所屬組的句柄陣列。 |

**輸出(setGroupMembershipReturn)**

IPS API不會為此操作返迴響應。

## 範例 {#section-67b86d259df24938896fe19061845811}

此代碼示例使用戶成為組的成員。 使用組句柄陣列將用戶添加到多個組。

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
