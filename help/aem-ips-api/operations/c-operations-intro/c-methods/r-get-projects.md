---
description: 獲取一組相關資產的項目。
solution: Experience Manager
title: getProjects
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d7262ed7-7419-4d6b-86ed-f3ad4657d654
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 22%

---

# getProjects{#getprojects}

獲取一組相關資產的項目。

語法

## 授權用戶類型 {#section-337649866b1f4098844d1974ed7ab5d0}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-8d549237b8c440b4872a0a086ddc00a1}

**輸入(getProjectsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 公司的把手。 |

**輸出(getProjectsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| projectArray | `types:ProjectArray` | 是 | 與公司關聯的項目陣列。 |

## 範例 {#section-8b12d0b948f644f68bf9a16060d3849a}

此代碼示例返回項目陣列中的所有項目句柄。

**請求**

```java
<ns1:getProjectsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getProjectsParam>
```

**回答**

```java
<getProjectsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <projectArray>
      <items>
         <projectHandle>47|My Project 1</projectHandle>
         <name>My Project 1</name>
      </items>
      <items>
         <projectHandle>47|My Project 2</projectHandle>
         <name>My Project 2</name>
      </items>
   </projectArray>
</getProjectsReturn>
```
