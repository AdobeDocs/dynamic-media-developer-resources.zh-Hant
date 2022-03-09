---
description: 更名項目。
solution: Experience Manager
title: 更名項目
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 1bf74ebf-1fce-408b-9953-7fdf2ae9d10b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 23%

---

# 更名項目{#renameproject}

更名項目。

語法

## 授權用戶類型 {#section-093d1f611a1647568e885ddd842b8f78}

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
| 公司名稱 | `xsd:string` | 是 | 處理要更名的項目的公司。 |
| 項目句柄 | `xsd:string` | 是 | 處理項目。 |
| 項目名稱 | `xsd:string` | 是 | 新建項目名稱。 |

**輸出(renameProjectParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 項目句柄 | `xsd:string` | 是 | 更名項目的句柄。 |

## 範例 {#section-a0a06d9244774795b695a10b92b2a5e7}

此代碼示例更名項目並返回項目句柄。

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
