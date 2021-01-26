---
description: 透過比較資產名稱與公司的影像伺服／影像轉換目錄名稱空間中的所有名稱，檢查IPS ID衝突。
seo-description: 透過比較資產名稱與公司的影像伺服／影像轉換目錄名稱空間中的所有名稱，檢查IPS ID衝突。
seo-title: checkAssetNames
solution: Experience Manager
title: checkAssetNames
topic: Dynamic Media Image Production System API
uuid: 91d073a8-7648-429b-aa5c-c7d595550299
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 10%

---


# checkAssetNames{#checkassetnames}

透過比較資產名稱與公司的影像伺服／影像轉換目錄名稱空間中的所有名稱，檢查IPS ID衝突。

語法

## 授權用戶類型{#section-8efcbb3f555f417a870219e4714374db}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## 參數{#section-9c75b00f2072453abea0bdefc6ad7c99}

**輸入(checkAssetNamesParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 否 | 包含使用者之公司的控制代碼。 |
| `*`assetNamesArray`*` | `types:StringArray` | 是 | 要檢查的資產名稱陣列。 |

**輸出(checkAssetNamesReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`inUseNameArray`*` | `types:StringArray` | 是 | 使用中的資產名稱陣列。 |

## 範例 {#section-bc5d120d74614a63a425ca3acc337219}

此范常式式碼會要求指定公司使用的資產名稱。 回應會傳回使用中的資產名稱陣列。

**請求**

```java
<checkAssetNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <companyHandle>c|1</companyHandle>
   <assetNameArray>
      <items>ABC123</items>
      <items>DEF456</items>
   </assetNameArray>
</checkAssetNamesParam>
```

**回答**

```java
<checkAssetNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <inUseNameArray>
      <items>DEF456</items>
   </inUseNameArray>
</checkAssetNamesReturn>
```

