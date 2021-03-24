---
description: 在單一請求中擷取所有系統屬性。
solution: Experience Manager
title: getSystemProperties
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 17%

---


# getSystemProperties{#getsystemproperties}

在單一請求中擷取所有系統屬性。

語法

## 授權用戶類型{#section-fc311ce90a54400fa95b9dd36b756e23}

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

此代碼示例返回系統屬性的陣列。 回應因簡短而截斷。

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

