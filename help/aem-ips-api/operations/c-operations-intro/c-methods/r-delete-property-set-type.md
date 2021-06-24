---
description: 刪除屬性集類型及其關聯的屬性集和屬性。
solution: Experience Manager
title: deletePropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 97ec0f41-794f-4340-b86d-ab07a742d447
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 11%

---

# deletePropertySetType{#deletepropertysettype}

刪除屬性集類型及其關聯的屬性集和屬性。

語法

## 授權的使用者類型 {#section-16a17b4ebf9a4639bdb2784a2e9fe00d}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-1c8973f5d35f44b4a6a483a41609e455}

**輸入(deletePropertySetTypeParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`typeHandle`*` | `xsd:string` | 是 | 要刪除的屬性集類型的句柄。 |

**輸出(deletePropertySetTypeParam)**

IPS API不會針對此操作傳回回應。

## 範例 {#section-85faa2e3411a4e23aa6489037f7ce078}

此代碼示例將類型的句柄用作發送到IPS Web服務伺服器的`deletePropertySetTypeParam`中的欄位，以刪除屬性集類型。

**請求**

```java
<deletePropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</deletePropertySetTypeParam>
```

**回答**

無。
