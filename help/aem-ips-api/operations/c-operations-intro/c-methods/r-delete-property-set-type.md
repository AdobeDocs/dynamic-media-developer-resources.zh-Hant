---
description: 刪除屬性集類型及其關聯的屬性集和屬性。
seo-description: 刪除屬性集類型及其關聯的屬性集和屬性。
seo-title: deletePropertySetType
solution: Experience Manager
title: deletePropertySetType
topic: Scene7 Image Production System API
uuid: 7a5232cc-fa3a-4dac-bf88-8b954dd37c87
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# deletePropertySetType{#deletepropertysettype}

刪除屬性集類型及其關聯的屬性集和屬性。

語法

## 授權使用者類型 {#section-16a17b4ebf9a4639bdb2784a2e9fe00d}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-1c8973f5d35f44b4a6a483a41609e455}

**輸入(deletePropertySetTypeParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`typeHandle`*` | `xsd:string` | 是 | 要刪除的屬性集類型的句柄。 |

**輸出(deletePropertySetTypeParam)**

IPS API不會傳回此作業的回應。

## 範例 {#section-85faa2e3411a4e23aa6489037f7ce078}

此程式碼範例會將類型的控制代碼當做傳送至IPS Web `deletePropertySetTypeParam` services伺服器的欄位，以刪除屬性集類型。

**請求**

```java
<deletePropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</deletePropertySetTypeParam>
```

**回答**

無。
