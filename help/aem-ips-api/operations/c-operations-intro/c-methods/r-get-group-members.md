---
description: 取得屬於特定公司和群組的使用者。
seo-description: 取得屬於特定公司和群組的使用者。
seo-title: getGroupMembers
solution: Experience Manager
title: getGroupMembers
topic: Scene7 Image Production System API
uuid: 02322b66-1c0c-4d84-a3eb-97a4fb605318
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 16%

---


# getGroupMembers{#getgroupmembers}

取得屬於特定公司和群組的使用者。

語法

## 授權用戶類型{#section-08a73460d122480292205bb8f2df9220}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-b798b06354c946abbb90fa72cc9c67fd}

**輸入(getGroupMembersParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 公司的把手。 |
| ` *`groupHandle`*` | `xsd:string` |  | 群組的控點。 |

**輸出(getGroupMembersReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`userHandleArray`*` | `type:HandleArray` | 是 | 一組用戶句柄。 |

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

