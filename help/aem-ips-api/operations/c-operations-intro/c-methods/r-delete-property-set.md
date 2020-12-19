---
description: 刪除屬性集和所有相關屬性。
seo-description: 刪除屬性集和所有相關屬性。
seo-title: deletePropertySet
solution: Experience Manager
title: deletePropertySet
topic: Scene7 Image Production System API
uuid: b4fdf51f-89ec-4a69-9179-078ee8e1937f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 11%

---


# deletePropertySet{#deletepropertyset}

刪除屬性集和所有相關屬性。

語法

## 授權用戶類型{#section-b54aa8c854de400a989b4957412ff42c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-e5fc868f69494cf6858e03027db09101}

**輸入(deletePropertySetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`setHandle`*` | `xsd:string` | 是 | 要刪除的屬性集的句柄。 |

**輸出(deletePropertySetParam)**

IPS API不會傳回此作業的回應。

## 範例 {#section-cf319fc8f86a40ab9cbd838b031973fe}

此程式碼範例會將集的控制代碼當做傳送至IPS Web伺服器的`deletePropertySetParam`欄位，以刪除屬性集。

**請求**

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**回答**

無。
