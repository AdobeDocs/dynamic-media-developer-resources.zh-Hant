---
description: 將來自特定公司的使用者新增至特定群組。
solution: Experience Manager
title: addGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c03525e3-6bc4-4c6a-bb5b-b0cb2e6f6d0d
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 10%

---

# addGroupMembers{#addgroupmembers}

將來自特定公司的使用者新增至特定群組。

語法

## 授權的使用者型別 {#section-b4406c54ed7c4827be4c1acc957e0057}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-b28434dcf2ca4b4ea431136aac33913e}

**輸入(addGroupMembersParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司的控制代碼。 |
| groupHandle | `xsd:string` | 是 | 群組控制代碼。 |
| userHandleArray | `types:HandleArray` | 是 | 您要新增至群組的使用者之控制代碼陣列。 |

**輸出(addGroupMembersParam)**

IPS API未傳回此作業的回應。

## 範例 {#section-8f168b528aef4c4fa8c3d41f7686842f}

此範例使用addGroupMembersParam將使用者新增至單一公司。 IPS API未傳回此作業的回應。

**要求**

```java {.line-numbers}
<ns1:addGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
<ns1:userHandleArray><ns1:items>70|kmagnusson@adobe.com</ns1:items></ns1:userHandleArray>
</ns1:addGroupMembersParam>
```

**回應**

無。
