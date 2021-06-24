---
description: 設定資產的影像對應。
solution: Experience Manager
title: setImageMaps
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 0c8e6536-0b9c-4fcc-b71f-511afc670089
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 10%

---

# setImageMaps{#setimagemaps}

設定資產的影像對應。

您必須已建立影像映射。 影像映射按從陣列中檢索的順序應用。 這表示第二個影像地圖會覆蓋第一個影像，第三個影像覆蓋第二個影像，以此類推。

## 授權的使用者類型 {#section-adb21c5b679249939dd83816e4a0ee97}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-2292ec1aead947ef8741dd0653a41f42}

**輸入(setImageMapsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司負責人。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 資產控制代碼。 |
| `*`imageMapArray`*` | `types:ImageMapDefinitionArray` | 是 | 預先定義的影像映射陣列。 |

**輸出(setImageMapsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`imageMapHandleArray`*` | `types:HandleArray` | 是 | 陣列，其中影像映射控點已套用至資產。 |

## 範例 {#section-fe2e35662a6a4ee29cf250c9fd180371}

此程式碼範例會為影像資產設定2個影像地圖。 該代碼指定調用影像映射時所採取的形狀類型、區域和操作。 回應包含一個陣列，內含影像映射的控點。

**請求**

```java
<setImageMapsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|739|1|537</assetHandle>
   <imageMapArray>
      <items>
         <name>ImageMap2</name>
         <shapeType>Rectangle</shapeType>
         <region>40</region>
         <action>400</action>
         <enabled>true</enabled>
      </items>
      <items>
         <name>ImageMap3</name>
         <shapeType>Rectangle</shapeType>
         <region>40</region>
         <action>400</action>
         <enabled>false</enabled>
      </items>
   </imageMapArray>
</setImageMapsParam>
```
