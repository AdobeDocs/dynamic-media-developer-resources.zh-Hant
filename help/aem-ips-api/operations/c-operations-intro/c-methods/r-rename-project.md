---
description: 重新命名專案。
solution: Experience Manager
title: renameProject
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 21%

---


# renameProject{#renameproject}

重新命名專案。

語法

## 授權用戶類型{#section-093d1f611a1647568e885ddd842b8f78}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-43ccd77648784be4a259a723c3e1db40}

**輸入(renameProjectParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyName`*` | `xsd:string` | 是 | 處理您要重新命名之專案所在的公司。 |
| `*`projectHandle`*` | `xsd:string` | 是 | 處理專案。 |
| `*`projectName`*` | `xsd:string` | 是 | 新專案名稱。 |

**輸出(renameProjectParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`projectHandle`*` | `xsd:string` | 是 | 已重新命名專案的控制代碼。 |

## 範例 {#section-a0a06d9244774795b695a10b92b2a5e7}

此程式碼範例會重新命名專案，並傳回專案控制代碼。

**請求**

```java
<renameProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ApiTestProject</projectHandle>
   <projectName>ProjectTestAPI</projectName>
</renameProjectParam>
```

**回答**

```java
<renameProjectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
</renameProjectReturn>
```

