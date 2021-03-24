---
description: 設定資產的影像地圖。
solution: Experience Manager
title: setImageMaps
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 10%

---


# setImageMaps{#setimagemaps}

設定資產的影像地圖。

您必須已建立影像地圖。 影像地圖會依從陣列擷取的順序套用。 這表示第二個影像地圖會覆蓋第一個影像地圖，第三個影像地圖會覆蓋第二個影像地圖，依此類推。

## 授權用戶類型{#section-adb21c5b679249939dd83816e4a0ee97}

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
| `*`imageMapArray`*` | `types:ImageMapDefinitionArray` | 是 | 預先定義的影像地圖陣列。 |

**輸出(setImageMapsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`imageMapHandleArray`*` | `types:HandleArray` | 是 | 具有映像映射句柄的陣列應用於資產。 |

## 範例 {#section-fe2e35662a6a4ee29cf250c9fd180371}

此程式碼範例會為影像資產設定2個影像地圖。 程式碼會指定在呼叫影像地圖時所採取的形狀類型、區域和動作。 響應包含一個具有影像映射句柄的陣列。

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

