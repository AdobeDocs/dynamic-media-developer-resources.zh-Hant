---
description: 刪除屬性集和所有關聯屬性。
solution: Experience Manager
title: deletePropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 72429030-200d-4e13-a537-10a728998a26
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 12%

---

# deletePropertySet{#deletepropertyset}

刪除屬性集和所有關聯屬性。

語法

## 授權的使用者類型 {#section-b54aa8c854de400a989b4957412ff42c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-e5fc868f69494cf6858e03027db09101}

**輸入(deletePropertySetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`setHandle`*` | `xsd:string` | 是 | 要刪除的屬性集的句柄。 |

**輸出(deletePropertySetParam)**

IPS API不會針對此操作傳回回應。

## 範例 {#section-cf319fc8f86a40ab9cbd838b031973fe}

此代碼示例將集的句柄用作發送到IPS Web服務伺服器的`deletePropertySetParam`中的欄位，以刪除該屬性集。

**請求**

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**回答**

無。
