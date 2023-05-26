---
description: 取得一組相關資產的專案。
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

取得一組相關資產的專案。

語法

## 授權的使用者型別 {#section-337649866b1f4098844d1974ed7ab5d0}

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
| companyHandle | `xsd:string` | 是 | 公司的控制代碼。 |

**輸出(getProjectsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| projectArray | `types:ProjectArray` | 是 | 與公司相關聯的專案陣列。 |

## 範例 {#section-8b12d0b948f644f68bf9a16060d3849a}

此程式碼範例會傳回專案陣列中的所有專案控制點。

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
