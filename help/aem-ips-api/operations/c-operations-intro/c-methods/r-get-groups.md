---
description: 傳回公司群組。
seo-description: 傳回公司群組。
seo-title: getGroups
solution: Experience Manager
title: getGroups
topic: Scene7 Image Production System API
uuid: d6e1542d-83a2-4b25-a986-2465e9e5a145
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 21%

---


# getGroups{#getgroups}

傳回公司群組。

語法

## 授權用戶類型{#section-27c77680a2f34e2f9ecd0af4ebb6847e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-0e06195f23dd4c69922df210f566dd18}

**輸入(getGroupsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 公司的把手。 |

**輸出(getGroupsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`groupArray`*` | `types:GroupArray` | 是 | 群組陣列。 |

## 範例 {#section-ed0708f611574354bf0c6ea83912b531}

此程式碼會傳回一個陣列，其中包含屬於特定公司的所有群組以及每個群組的特定資訊。

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

