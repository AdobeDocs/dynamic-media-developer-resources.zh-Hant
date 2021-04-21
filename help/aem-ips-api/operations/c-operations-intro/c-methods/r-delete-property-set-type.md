---
description: 刪除屬性集類型及其關聯的屬性集和屬性。
solution: Experience Manager
title: deletePropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 11%

---


# deletePropertySetType{#deletepropertysettype}

刪除屬性集類型及其關聯的屬性集和屬性。

語法

## 授權用戶類型{#section-16a17b4ebf9a4639bdb2784a2e9fe00d}

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

IPS API不會傳回此作業的回應。

## 範例 {#section-85faa2e3411a4e23aa6489037f7ce078}

此程式碼範例會將類型的控制代碼當做傳送至IPS Web services伺服器的`deletePropertySetTypeParam`欄位，以刪除屬性集類型。

**請求**

```java
<deletePropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</deletePropertySetTypeParam>
```

**回答**

無。
