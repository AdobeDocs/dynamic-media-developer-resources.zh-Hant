---
description: 刪除屬性集類型及其關聯的屬性集和屬性。
solution: Experience Manager
title: deletePropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 97ec0f41-794f-4340-b86d-ab07a742d447
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 11%

---

# deletePropertySetType{#deletepropertysettype}

刪除屬性集類型及其關聯的屬性集和屬性。

語法

## 授權用戶類型 {#section-16a17b4ebf9a4639bdb2784a2e9fe00d}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-1c8973f5d35f44b4a6a483a41609e455}

**Input(deletePropertySetTypeParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 類型句柄 | `xsd:string` | 是 | 要刪除的屬性集類型的句柄。 |

**輸出(deletePropertySetTypeParam)**

IPS API不會為此操作返迴響應。

## 範例 {#section-85faa2e3411a4e23aa6489037f7ce078}

此代碼示例將類型的句柄用作 `deletePropertySetTypeParam` 發送到IPS Web服務伺服器以刪除屬性集類型。

**請求**

```java
<deletePropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</deletePropertySetTypeParam>
```

**回答**

無。
