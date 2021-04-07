---
description: 屬性集類型指定用於幫助管理屬性集的各種設定。
solution: Experience Manager
title: createPropertySetType
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
exl-id: 1730ccbf-e8b0-4f92-9daf-da2fa047cbbd
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 10%

---

# createPropertySetType{#createpropertysettype}

屬性集類型指定用於幫助管理屬性集的各種設定。

語法

## 授權用戶類型{#section-48e5f908276c4a549fd33a8828bad326}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-43dece72eb9f44df80f4a119dd2c008b}

**輸入(createPropertySetTypeParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 否 | 擁有屬性集類型的公司的句柄。 如果`companyHandle`未傳遞，而呼叫者是`IpsAdmin`，則會建立全局屬性集類型。 |
| `*`名稱`*` | `xsd:string` | 是 | 屬性集類型的名稱。 |
| `*`propertyType`*` | `xsd:string` | 是 | 屬性集類型的選擇。 |
| `*`allowMultiple`*` | `xsd:boolean` | 是 | 確定程式是否可以有多個屬性集。 |

**輸出(createPropertySetTypeReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`typeHandle`*` | `xsd:string` | 是 | 類型的控點。 |

## 範例 {#section-13396c9639a6475190e622eae3cdb534}

此代碼示例建立一個屬性集，其名稱和類型由`PropertySet Types`常數指定。 擁有屬性集類型的公司的句柄。 如果未傳遞companyHandle，而呼叫者是IpsAdmin，則會建立全局屬性集類型。

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
