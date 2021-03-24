---
description: 使用屬性陣列更新屬性集。
solution: Experience Manager
title: updatePropertySet
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 14%

---


# updatePropertySet{#updatepropertyset}

使用屬性陣列更新屬性集。

語法

## 授權用戶類型{#section-116693bbfb5d44219e62bbb1ba19de96}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-98361b063e9c41e8b2f744fabc0e13ed}

**Input(updatePropertySetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`setHandle`*` | `xsd:string` | 是 | 屬性集的句柄。 |
| `*`replaceProperties`*` | `xsd:string` | 否 | 設為`true`以取代屬性。 |
| `*`propertyArray`*` | `types:PropertyArray` | 是 | 屬性集的更新屬性陣列。 |

**Output(updatePropertySetReturn)**

IPS API不會傳回此作業的回應。

## 範例 {#section-55d1c9dcd0174c6b9b52b4709f7c8bf9}

此程式碼範例會更新屬性陣列中具有屬性的屬性集。

**請求**

```java
<updatePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
   <replaceProperties>true</replaceProperties>
   <propertyArray>
      <items>
         <name>application_project_whatever</name>
         <value>false</value>
      </items>
      <items>
         <name>application_server_prefix_published_test</name>
         <value>http://s7teton.macromedia.com:8080/is/image/</value>
      </items>
      <items>
         <name>application_server_prefix_origin_test</name>
         <value>http://s7teton:8080/is/image/</value>
      </items>
   </propertyArray>
</updatePropertySetParam>
```

**回答**

無。
