---
description: 刪除屬性集型別及其關聯的屬性集和屬性。
solution: Experience Manager
title: deletePropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 97ec0f41-794f-4340-b86d-ab07a742d447
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 9%

---

# deletePropertySetType{#deletepropertysettype}

刪除屬性集型別及其關聯的屬性集和屬性。

語法

## 授權的使用者型別 {#section-16a17b4ebf9a4639bdb2784a2e9fe00d}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-1c8973f5d35f44b4a6a483a41609e455}

**輸入(deletePropertySetTypeParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| typeHandle | `xsd:string` | 是 | 要刪除的屬性集型別的控制代碼。 |

**輸出(deletePropertySetTypeParam)**

IPS API未傳回此作業的回應。

## 範例 {#section-85faa2e3411a4e23aa6489037f7ce078}

這個程式碼範例使用型別的控制代碼做為傳送至IPS Web服務伺服器之`deletePropertySetTypeParam`中的欄位，以刪除屬性集型別。

**要求**

```java
<deletePropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</deletePropertySetTypeParam>
```

**回應**

無。
