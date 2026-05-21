---
description: 比較資產名稱與公司影像伺服/影像轉譯目錄名稱空間的所有名稱，以檢查IPS ID衝突。
solution: Experience Manager
title: checkAssetName
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0756c4fc-64ec-4022-a6aa-fcf1542b41b0
TQID: 'https://experienceleague.adobe.com/RbFXhRqcaGXLMAeJhXMzho-ylSe2ktcKwvdbFtrcppM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 11%

---

# checkAssetName{#checkassetnames}

比較資產名稱與公司影像伺服/影像轉譯目錄名稱空間的所有名稱，以檢查IPS ID衝突。

語法

## 授權的使用者型別 {#section-8efcbb3f555f417a870219e4714374db}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## 引數 {#section-9c75b00f2072453abea0bdefc6ad7c99}

**輸入(checkAssetNamesParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 否 | 包含使用者的公司的控制代碼。 |
| assetNamesArray | `types:StringArray` | 是 | 要檢查的資產名稱陣列。 |

**輸出(checkAssetNamesReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| inUseNameArray | `types:StringArray` | 是 | 使用中的資產名稱陣列。 |

## 範例 {#section-bc5d120d74614a63a425ca3acc337219}

此範常式式碼會要求指定公司使用中的資產名稱。 回應會傳回使用中的資產名稱陣列。

**要求**

```java
<checkAssetNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <companyHandle>c|1</companyHandle>
   <assetNameArray>
      <items>ABC123</items>
      <items>DEF456</items>
   </assetNameArray>
</checkAssetNamesParam>
```

**回應**

```java
<checkAssetNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <inUseNameArray>
      <items>DEF456</items>
   </inUseNameArray>
</checkAssetNamesReturn>
```
