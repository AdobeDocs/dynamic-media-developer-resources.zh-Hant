---
description: 建立新項目。
solution: Experience Manager
title: 建立項目
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dd9c07df-9a8f-4b67-9838-31dd96fd127b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 19%

---

# 建立項目{#createproject}

建立新項目。

語法

## 授權用戶類型 {#section-17878e2e4c3a44988c9a1af82c2ac319}

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
| 公司句柄 | `xsd:string` | 是 | 與新項目關聯的公司的句柄。 |
| 項目名稱 | `xsd:string` | 是 | 新建項目名稱。 |

**輸出(createProjectParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 項目句柄 | `xsd:string` | 是 | 新項目的句柄。 |

## 範例 {#section-a0cd532b67e346d088fbec141231a0e5}

此代碼示例建立名為 `ApiTestProject` 在其句柄指定的公司中。 響應將句柄返回到項目。

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
