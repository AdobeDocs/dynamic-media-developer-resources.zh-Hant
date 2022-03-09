---
description: 獲取與類型句柄關聯的屬性集。
solution: Experience Manager
title: getPropertySets
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: da6923c3-9b86-4595-8205-645fb10e03b0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 18%

---

# getPropertySets{#getpropertysets}

獲取與類型句柄關聯的屬性集。

語法

## 授權用戶類型 {#section-da858360b72941bfa8d9558b4da7d4da}

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

**Input(getPropertySetsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 類型句柄 | `xsd:string` | 是 | 屬性集類型的句柄。 |
| primaryOwnerHandle | `xsd:string` | 是 | 綁定到資料庫對象的資料的主所有者。 |
| secondaryOwnerHandle | `xsd:string` | 否 | 資料的可選輔助所有者。 |

**輸出(getPropertySetsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| setArray | `types:PropertySetArray` | 是 | 屬性集的陣列。 |

## 範例 {#section-1358af974eab4259864910337a6f0bd2}

此代碼示例返回由類型句柄指定的其主要所有者的屬性集。

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
