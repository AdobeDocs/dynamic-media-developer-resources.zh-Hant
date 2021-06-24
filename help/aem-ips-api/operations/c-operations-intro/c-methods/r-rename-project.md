---
description: 重新命名專案。
solution: Experience Manager
title: renameProject
feature: Dynamic Media Classic,SDK/API，資產管理
role: Developer,Administrator
exl-id: 1bf74ebf-1fce-408b-9953-7fdf2ae9d10b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 21%

---

# renameProject{#renameproject}

重新命名專案。

語法

## 授權的使用者類型 {#section-093d1f611a1647568e885ddd842b8f78}

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
| `*`companyName`*` | `xsd:string` | 是 | 使用您要重新命名的專案處理公司。 |
| `*`projectHandle`*` | `xsd:string` | 是 | 處理專案。 |
| `*`projectName`*` | `xsd:string` | 是 | 新專案名稱。 |

**輸出(renameProjectParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`projectHandle`*` | `xsd:string` | 是 | 已重新命名專案的控制代碼。 |

## 範例 {#section-a0a06d9244774795b695a10b92b2a5e7}

此程式碼範例會重新命名專案並傳回專案控制代碼。

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
