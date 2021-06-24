---
description: 將資產名稱與公司的影像伺服/影像轉譯目錄命名空間中的所有名稱進行比較，以檢查IPS ID衝突。
solution: Experience Manager
title: checkAssetNames
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 0756c4fc-64ec-4022-a6aa-fcf1542b41b0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 12%

---

# checkAssetNames{#checkassetnames}

將資產名稱與公司的影像伺服/影像轉譯目錄命名空間中的所有名稱進行比較，以檢查IPS ID衝突。

語法

## 授權的使用者類型 {#section-8efcbb3f555f417a870219e4714374db}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## 參數 {#section-9c75b00f2072453abea0bdefc6ad7c99}

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

此范常式式碼會要求指定公司使用中的資產名稱。 回應會傳回使用中的資產名稱陣列。

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
