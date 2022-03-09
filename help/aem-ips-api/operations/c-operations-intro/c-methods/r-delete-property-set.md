---
description: 刪除屬性集和所有關聯屬性。
solution: Experience Manager
title: deletePropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 72429030-200d-4e13-a537-10a728998a26
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 13%

---

# deletePropertySet{#deletepropertyset}

刪除屬性集和所有關聯屬性。

語法

## 授權用戶類型 {#section-b54aa8c854de400a989b4957412ff42c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-e5fc868f69494cf6858e03027db09101}

**Input(deletePropertySetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| setHandle | `xsd:string` | 是 | 要刪除的屬性集的句柄。 |

**輸出(deletePropertySetParam)**

IPS API不會為此操作返迴響應。

## 範例 {#section-cf319fc8f86a40ab9cbd838b031973fe}

此代碼示例將集的句柄用作 `deletePropertySetParam` 發送到IPS Web服務伺服器以刪除屬性集。

**請求**

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**回答**

無。
