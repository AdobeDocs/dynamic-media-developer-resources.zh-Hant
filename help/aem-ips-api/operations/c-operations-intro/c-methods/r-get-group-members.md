---
description: 取得屬於特定公司和群組的使用者。
solution: Experience Manager
title: getGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 81af79ee-be82-439f-9f42-a1ec09cd8ea0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 17%

---

# getGroupMembers{#getgroupmembers}

取得屬於特定公司和群組的使用者。

語法

## 授權的使用者類型 {#section-08a73460d122480292205bb8f2df9220}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-b798b06354c946abbb90fa72cc9c67fd}

**輸入(getGroupMembersParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司的把手。 |
| `*`groupHandle`*` | `xsd:string` |  | 組的句柄。 |

**輸出(getGroupMembersReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`userHandleArray`*` | `type:HandleArray` | 是 | 用戶句柄的陣列。 |

## 範例 {#section-aaa340dba6b64cce9bcd8303cf999166}

此程式碼範例會傳回包含屬於特定群組之所有使用者的使用者控制代碼陣列。

**請求**

```java
<ns1:getGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
</ns1:getGroupMembersParam>
```

**回答**

```java
<getGroupMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userHandleArray>
      <items>70|kmagnusson@adobe.com</items>
   </userHandleArray>
</getGroupMembersReturn>
```
