---
description: 將特定公司的用戶添加到特定組。
solution: Experience Manager
title: addGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c03525e3-6bc4-4c6a-bb5b-b0cb2e6f6d0d
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 12%

---

# addGroupMembers{#addgroupmembers}

將特定公司的用戶添加到特定組。

語法

## 授權用戶類型 {#section-b4406c54ed7c4827be4c1acc957e0057}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-b28434dcf2ca4b4ea431136aac33913e}

**Input(addGroupMembersParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 公司的把手。 |
| 組句柄 | `xsd:string` | 是 | 組句柄。 |
| userHandleArray | `types:HandleArray` | 是 | 要添加到組的用戶的句柄陣列。 |

**輸出(addGroupMembersParam)**

IPS API不會為此操作返迴響應。

## 範例 {#section-8f168b528aef4c4fa8c3d41f7686842f}

此示例使用addGroupMembersParam將用戶添加到單個公司。 IPS API不會為此操作返迴響應。

**請求**

```java {.line-numbers}
<ns1:addGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
<ns1:userHandleArray><ns1:items>70|kmagnusson@adobe.com</ns1:items></ns1:userHandleArray>
</ns1:addGroupMembersParam>
```

**回答**

無。
