---
description: 取得一組相關資產的專案。
seo-description: 取得一組相關資產的專案。
seo-title: getProjects
solution: Experience Manager
title: getProjects
topic: Scene7 Image Production System API
uuid: 46ec9a5d-4414-4c9c-aaf2-0db654204b61
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getProjects{#getprojects}

取得一組相關資產的專案。

語法

## 授權使用者類型 {#section-337649866b1f4098844d1974ed7ab5d0}

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
| ` *`companyHandle`*` | `xsd:string` | 是 | 公司的把手。 |

**輸出(getProjectsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`projectArray`*` | `types:ProjectArray` | 是 | 與公司關聯的專案陣列。 |

## 範例 {#section-8b12d0b948f644f68bf9a16060d3849a}

此程式碼範例會傳回專案陣列中的所有專案控制代碼。

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

