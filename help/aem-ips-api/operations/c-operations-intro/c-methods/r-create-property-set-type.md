---
description: 屬性集類型指定用於幫助管理屬性集的各種設定。
solution: Experience Manager
title: createPropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1730ccbf-e8b0-4f92-9daf-da2fa047cbbd
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 12%

---

# createPropertySetType{#createpropertysettype}

屬性集類型指定用於幫助管理屬性集的各種設定。

語法

## 授權用戶類型 {#section-48e5f908276c4a549fd33a8828bad326}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-43dece72eb9f44df80f4a119dd2c008b}

**Input(createPropertySetTypeParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`公司句柄`*` | `xsd:string` | 否 | 擁有屬性集類型的公司的句柄。 如果 `companyHandle` 未傳遞，呼叫者是 `IpsAdmin`，將建立全局屬性集類型。 |
| `*`名稱`*` | `xsd:string` | 是 | 屬性集類型的名稱。 |
| `*`屬性類型`*` | `xsd:string` | 是 | 屬性集類型的選擇。 |
| `*`允許多個`*` | `xsd:boolean` | 是 | 確定程式是否可以具有多個屬性集。 |

**輸出(createPropertySetTypeReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`類型句柄`*` | `xsd:string` | 是 | 類型的句柄。 |

## 範例 {#section-13396c9639a6475190e622eae3cdb534}

此代碼示例建立具有由 `PropertySet Types` 常數。 擁有屬性集類型的公司的句柄。 如果未傳遞companyHandle且調用方為IpsAdmin，則會建立全局屬性集類型。

**請求**

```java
<createPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10803</typeHandle>
</createPropertySetTypeReturn>
```

**回答**

```java
<createPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</createPropertySetTypeReturn>
```
