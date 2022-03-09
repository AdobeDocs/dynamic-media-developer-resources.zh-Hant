---
description: 設定資產的影像映射。
solution: Experience Manager
title: setImageMaps
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0c8e6536-0b9c-4fcc-b71f-511afc670089
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 11%

---

# setImageMaps{#setimagemaps}

設定資產的影像映射。

您必須已建立映像映射。 以從陣列檢索的順序應用影像映射。 這意味著第二影像圖疊加第一影像圖，第三影像圖疊加第二影像圖等。

## 授權用戶類型 {#section-adb21c5b679249939dd83816e4a0ee97}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-2292ec1aead947ef8741dd0653a41f42}

**Input(setImageMapsParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 公司負責。 |
| 資產句柄 | `xsd:string` | 是 | 資產句柄。 |
| imageMapArray | `types:ImageMapDefinitionArray` | 是 | 預定義影像映射的陣列。 |

**輸出(setImageMapsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| imageMapHandleArray | `types:HandleArray` | 是 | 具有應用於資產的影像映射句柄的陣列。 |

## 範例 {#section-fe2e35662a6a4ee29cf250c9fd180371}

此代碼示例為影像資產設定2個影像映射。 代碼指定調用影像映射時所採取的形狀類型、區域和操作。 該響應包含一個包含影像映射句柄的陣列。

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
