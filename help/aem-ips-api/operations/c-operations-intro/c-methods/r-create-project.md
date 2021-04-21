---
description: 建立新專案。
solution: Experience Manager
title: createProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 18%

---


# createProject{#createproject}

建立新專案。

語法

## 授權用戶類型{#section-17878e2e4c3a44988c9a1af82c2ac319}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-8c741884eb54489bbaad0c444fee80b6}

**輸入(createProjectParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 與新項目關聯的公司的控制代碼。 |
| `*`projectName`*` | `xsd:string` | 是 | 新專案名稱。 |

**輸出(createProjectParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`projectHandle`*` | `xsd:string` | 是 | 新專案的控制代碼。 |

## 範例 {#section-a0cd532b67e346d088fbec141231a0e5}

此代碼示例在由其句柄指定的公司中建立名為`ApiTestProject`的項目。 回應會將控制代碼傳回至專案。

**請求**

```java
<createProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectName>ApiTestProject</projectName>
</createProjectParam>
```

```java
<createProjectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <projectHandle>p|6|ApiTestProject</projectHandle>
</createProjectReturn>
```

