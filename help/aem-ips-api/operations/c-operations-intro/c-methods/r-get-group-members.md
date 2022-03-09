---
description: 獲取屬於特定公司和組的用戶。
solution: Experience Manager
title: getGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81af79ee-be82-439f-9f42-a1ec09cd8ea0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 18%

---

# getGroupMembers{#getgroupmembers}

獲取屬於特定公司和組的用戶。

語法

## 授權用戶類型 {#section-08a73460d122480292205bb8f2df9220}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-b798b06354c946abbb90fa72cc9c67fd}

**輸入(getGroupMembersParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 公司的把手。 |
| 組句柄 | `xsd:string` |  | 組的句柄。 |

**輸出(getGroupMembersReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| userHandleArray | `type:HandleArray` | 是 | 用戶句柄陣列。 |

## 範例 {#section-aaa340dba6b64cce9bcd8303cf999166}

此代碼示例返回包含屬於特定組的所有用戶的用戶句柄陣列。

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
