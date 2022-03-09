---
description: 通過將資產名稱與公司的Image Serving/Image Rendering目錄命名空間的所有名稱進行比較，檢查IPS ID衝突。
solution: Experience Manager
title: checkAssetNames
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0756c4fc-64ec-4022-a6aa-fcf1542b41b0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 12%

---

# checkAssetNames{#checkassetnames}

通過將資產名稱與公司的Image Serving/Image Rendering目錄命名空間的所有名稱進行比較，檢查IPS ID衝突。

語法

## 授權用戶類型 {#section-8efcbb3f555f417a870219e4714374db}

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
| 公司句柄 | `xsd:string` | 否 | 包含用戶的公司的句柄。 |
| assetNamesArray | `types:StringArray` | 是 | 要檢查的資產名稱陣列。 |

**輸出(checkAssetNamesReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| inUseNameArray | `types:StringArray` | 是 | 正在使用的資產名稱陣列。 |

## 範例 {#section-bc5d120d74614a63a425ca3acc337219}

此示例代碼請求指定公司使用的資產名稱。 響應返回正在使用的資產名稱的陣列。

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
