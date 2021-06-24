---
description: 屬性集是特定於應用程式的名稱值對集，可以根據屬性集類型附加到各種IPS對象。 如果屬性集類型不允許將多個集附加到對象(PropertySetType/allowMultipleisfalse)，並且該對象已具有相同類型的關聯集，則新集將替換現有集。
solution: Experience Manager
title: createPropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: e9f85e65-4a2f-4b82-b7b8-d0d60b8345cd
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 8%

---

# createPropertySet{#createpropertyset}

屬性集是特定於應用程式的名稱值對集，可以根據屬性集類型附加到各種IPS對象。 如果屬性集類型不允許將多個集附加到對象(PropertySetType/allowMultipleisfalse)，並且該對象已具有相同類型的關聯集，則新集將替換現有集。

語法

## 授權的使用者類型 {#section-f9b6187ba636475787c997fc27bb192a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-25258e75f5f3419bad165c797eb6cd8e}

**輸入(createPropertySetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`typeHandle`*` | `xsd:string` | 是 | 屬性集類型的句柄。 |
| `*`primaryOwnerHandle`*` | `xsd:string` | 是 | 屬性集的主要所有者的句柄。 |
| `*`secondaryOwnerHandle`*` | `xsd:string` | 否 | 屬性集的次要所有者的句柄。 |
| `*`propertyArray`*` | `types:PropertyArray` | 是 | 屬性陣列。 |
| `*`permissionArray`*` | `types:PermissionUpdateArray` |  |  |

**輸出(createPropertySetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`setHandle`*` | `xsd:string` | 是 | 新屬性集的句柄。 |

## 範例 {#section-4e1f5b2883664bc88f590fcd253df22b}

此代碼示例建立包含屬性名稱和值的屬性集。 回應會傳回新屬性集的控制代碼。

**請求**

```java
<createPropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
   <primaryOwnerHandle>u|41|strangio@adobe.com</primaryOwnerHandle>
   <propertyArray>
      <items>
         <name>application_project_whatever</name>
         <value>true</value>
      </items>
      <items>
         <name>application_server_prefix_published_test</name>
         <value>http://s7everest.macromedia.com:8080/is/image/</value>
      </items>
      <items>
         <name>application_server_prefix_origin_test</name>
         <value>http://s7everest:8080/is/image/</value>
      </items>
   </propertyArray>
</createPropertySetParam>
```

**回答**

```java
<createPropertySetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</createPropertySetReturn>
```
