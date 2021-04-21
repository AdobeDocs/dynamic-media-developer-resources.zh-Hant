---
description: 將特定公司的使用者新增至特定群組。
solution: Experience Manager
title: addGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 12%

---


# addGroupMembers{#addgroupmembers}

將特定公司的使用者新增至特定群組。

語法

## 授權用戶類型{#section-b4406c54ed7c4827be4c1acc957e0057}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-b28434dcf2ca4b4ea431136aac33913e}

**輸入(addGroupMembersParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司的把手。 |
| `*`groupHandle`*` | `xsd:string` | 是 | 群組控制代碼。 |
| `*`userHandleArray`*` | `types:HandleArray` | 是 | 您要新增至群組的使用者的控制代碼陣列。 |

**輸出(addGroupMembersParam)**

IPS API不會傳回此作業的回應。

## 範例 {#section-8f168b528aef4c4fa8c3d41f7686842f}

此範例使用`*`addGroupMembersParam`*`將使用者新增至單一公司。 IPS API不會傳回此作業的回應。

**請求**

```java
<ns1:addGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
<ns1:userHandleArray><ns1:items>70|kmagnusson@adobe.com</ns1:items></ns1:userHandleArray>
</ns1:addGroupMembersParam>
```

**回答**

無。
