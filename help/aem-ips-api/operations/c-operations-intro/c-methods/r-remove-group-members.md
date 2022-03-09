---
description: 從特定組中刪除公司用戶。
solution: Experience Manager
title: 刪除組成員
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8a9b7d54-d11b-41a8-9783-573a316e0ac6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 10%

---

# 刪除組成員{#removegroupmembers}

從特定組中刪除公司用戶。

**刪除命令之間的差異**

* `removeGroupMembers`:從組中刪除多個用戶。
* `removeGroupMembership`:從一組組中刪除單個用戶。

## 授權用戶類型 {#section-2c64cdac15184fbba6c7b2945b5d87f7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-b5596614a3be4ce5962455884e4636af}

**Input(removeGroupMembersParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 與您要處理的用戶一起使用的公司的句柄。 |
| 組句柄 | `xsd:string` | 是 | 組句柄。 |
| userHandleArray | `types:HandleArray` | 是 | 要刪除其組成員身份的用戶的句柄陣列。 |

**輸出(removeGroupMembersParam)**

IPS API不會為此操作返迴響應。

## 範例 {#section-9eedac852cea46ec80de6a6928bf97ac}

此代碼示例將用戶從指定的公司中刪除。 使用用戶句柄陣列從組中刪除多個用戶。

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
