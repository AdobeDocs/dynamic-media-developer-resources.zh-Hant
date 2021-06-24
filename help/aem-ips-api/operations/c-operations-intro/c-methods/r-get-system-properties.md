---
description: 在單一請求中擷取所有系統屬性。
solution: Experience Manager
title: getSystemProperties
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: b0ef16fd-1645-4e22-99bb-8c9269623168
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 18%

---

# getSystemProperties{#getsystemproperties}

在單一請求中擷取所有系統屬性。

語法

## 授權的使用者類型 {#section-fc311ce90a54400fa95b9dd36b756e23}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## 參數 {#section-b2a4fb7068424223aec87c50f0586d73}

**輸入(getSystemPropertiesParam)**

無。

**輸出(getSystemPropertiesReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`propertyArray`*` | `types:PropertyArray` | 是 | 系統屬性的陣列。 |

## 範例 {#section-728cc16fe9954b2daa035b4d4d4b4ce6}

此程式碼範例會傳回系統屬性的陣列。 回應因簡單性而遭截斷。

**請求**

```java
<getSystemPropertiesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10"/>
```

**回答**

```java
<getSystemPropertiesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10"> 
   <propertyArray> 
      <items> 
         <name>SvgRenderEnabled</name> 
         <value>true</value> 
      </items> 
      <items> 
         <name>SwfRootUrl</name> 
         <value>/SWFs/</value> 
      </items> 
      ... 
   </propertyArray> 
</getSystemPropertiesReturn>
```
