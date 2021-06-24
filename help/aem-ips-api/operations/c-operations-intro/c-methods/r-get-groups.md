---
description: 傳回公司群組。
solution: Experience Manager
title: getGroups
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: d98c08a6-4c20-4538-9598-c905078ab7de
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 21%

---

# getGroups{#getgroups}

傳回公司群組。

語法

## 授權的使用者類型 {#section-27c77680a2f34e2f9ecd0af4ebb6847e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-0e06195f23dd4c69922df210f566dd18}

**輸入(getGroupsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司的把手。 |

**輸出(getGroupsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`groupArray`*` | `types:GroupArray` | 是 | 群組陣列。 |

## 範例 {#section-ed0708f611574354bf0c6ea83912b531}

此程式碼會傳回陣列，其中包含屬於特定公司的所有群組以及每個群組的特定資訊。

**請求**

```java
<ns1:getGroupsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getGroupsParam>
```

```java
<getGroupsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupArray>
      <items>
         <groupHandle>225</groupHandle>
         <companyHandle>47</companyHandle>
         <name>MyGroup</name>
         <isSystemDefined>false</isSystemDefined>
      </items>
   </groupArray>
</getGroupsReturn>
```
