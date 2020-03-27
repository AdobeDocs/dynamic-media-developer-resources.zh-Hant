---
description: 屬性集類型指定用於幫助管理屬性集的各種設定。
seo-description: 屬性集類型指定用於幫助管理屬性集的各種設定。
seo-title: createPropertySetType
solution: Experience Manager
title: createPropertySetType
topic: Scene7 Image Production System API
uuid: ecbaad48-d725-4f7a-a37d-5e4cde3295cb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# createPropertySetType{#createpropertysettype}

屬性集類型指定用於幫助管理屬性集的各種設定。

語法

## 授權使用者類型 {#section-48e5f908276c4a549fd33a8828bad326}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-43dece72eb9f44df80f4a119dd2c008b}

**輸入(createPropertySetTypeParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 否 | 擁有屬性集類型的公司的句柄。 如果 `companyHandle` 未傳遞呼叫者為呼叫者 `IpsAdmin`，則將建立全局屬性集類型。 |
| ` *`名稱`*` | `xsd:string` | 是 | 屬性集類型的名稱。 |
| ` *`propertyType`*` | `xsd:string` | 是 | 屬性集類型的選擇。 |
| ` *`allowMultiple`*` | `xsd:boolean` | 是 | 確定程式是否可以有多個屬性集。 |

**輸出(createPropertySetTypeReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`typeHandle`*` | `xsd:string` | 是 | 類型的控點。 |

## 範例 {#section-13396c9639a6475190e622eae3cdb534}

此代碼示例建立一個屬性集，其名稱和類型由常數指 `PropertySet Types` 定。 擁有屬性集類型的公司的句柄。 如果未傳遞companyHandle，而呼叫者是IpsAdmin，則會建立全局屬性集類型。

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

