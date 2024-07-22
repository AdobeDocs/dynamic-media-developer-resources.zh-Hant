---
description: 使用屬性陣列來更新屬性集。
solution: Experience Manager
title: updatePropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: bbe6a664-b6e1-4b46-867d-a134070b13da
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 12%

---

# updatePropertySet{#updatepropertyset}

使用屬性陣列來更新屬性集。

語法

## 授權的使用者型別 {#section-116693bbfb5d44219e62bbb1ba19de96}

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

**輸入(updatePropertySetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| setHandle | `xsd:string` | 是 | 屬性集的控制代碼。 |
| replaceProperties | `xsd:string` | 否 | 設定為`true`以取代屬性。 |
| propertyArray | `types:PropertyArray` | 是 | 屬性集的已更新屬性陣列。 |

**輸出(updatePropertySetReturn)**

IPS API未傳回此作業的回應。

## 範例 {#section-55d1c9dcd0174c6b9b52b4709f7c8bf9}

此程式碼範例會使用屬性陣列中的屬性來更新屬性集。

**要求**

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

**回應**

無。
