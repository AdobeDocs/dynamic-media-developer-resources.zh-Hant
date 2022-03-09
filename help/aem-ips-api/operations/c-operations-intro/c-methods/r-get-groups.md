---
description: 返回公司組。
solution: Experience Manager
title: get組
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d98c08a6-4c20-4538-9598-c905078ab7de
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 22%

---

# get組{#getgroups}

返回公司組。

語法

## 授權用戶類型 {#section-27c77680a2f34e2f9ecd0af4ebb6847e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 參數 {#section-0e06195f23dd4c69922df210f566dd18}

**輸入(getGroupsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 公司的把手。 |

**輸出(getGroupsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 組陣列 | `types:GroupArray` | 是 | 組陣列。 |

## 範例 {#section-ed0708f611574354bf0c6ea83912b531}

此代碼返回一個陣列，該陣列包含屬於特定公司的所有組以及每個組的特定資訊。

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
