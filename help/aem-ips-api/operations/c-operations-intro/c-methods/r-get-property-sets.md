---
description: 獲取與類型句柄關聯的屬性集。
solution: Experience Manager
title: getPropertySets
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: da6923c3-9b86-4595-8205-645fb10e03b0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 17%

---

# getPropertySets{#getpropertysets}

獲取與類型句柄關聯的屬性集。

語法

## 授權的使用者類型 {#section-da858360b72941bfa8d9558b4da7d4da}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-d8da2847e77e4a95a4441d9848cac775}

**輸入(getPropertySetsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`typeHandle`*` | `xsd:string` | 是 | 屬性集類型的句柄。 |
| `*`primaryOwnerHandle`*` | `xsd:string` | 是 | 綁定到資料庫對象的資料的主要所有者。 |
| `*`secondaryOwnerHandle`*` | `xsd:string` | 否 | 資料的可選次要擁有者。 |

**Output(getPropertySetsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`setArray`*` | `types:PropertySetArray` | 是 | 屬性集的陣列。 |

## 範例 {#section-1358af974eab4259864910337a6f0bd2}

此代碼示例返回其主要所有者的屬性集，由類型句柄指定。

**請求**

```java
<getPropertySetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
   <primaryOwnerHandle>u|41|strangio@adobe.com</primaryOwnerHandle>
</getPropertySetsParam>
```

**回答**

```java
<getPropertySetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setArray>
      <items>
         <setHandle>ps|941</setHandle>
         <typeHandle>pt|10801</typeHandle>
         <propertyArray>
            <items>
               <name>application_server_prefix_published_test</name>
               <value>http://s7teton.macromedia.com:8080/is/image/</value>
            </items>
            <items>
               <name>application_project_whatever</name>
               <value>false</value>
            </items>
            <items>
               <name>application_server_prefix_origin_test</name>
               <value>http://s7teton:8080/is/image</value>
            </items>
         </propertyArray>
      </items>
   </setArray>
</getPropertySetsReturn>
```
