---
description: 將資產移至特定資料夾。
seo-description: 將資產移至特定資料夾。
seo-title: moveAsset
solution: Experience Manager
title: moveAsset
topic: Scene7 Image Production System API
uuid: cabeb7b7-ab0b-44d0-ad90-623f76e4323d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 15%

---


# moveAsset{#moveasset}

將資產移至特定資料夾。

語法

## 授權用戶類型{#section-e4f2d2a58132450aa36da6377134211e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-dd0bbdf293aa4563af70a91f97c861f1}

**輸入(moveAssetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 為公司負責。 |
| ` *`assetHandle`*` | `xsd:string` | 是 | 處理您要移動的資產。 |
| ` *`folderHandle`*` | `xsd:string` | 是 | 目標資料夾的句柄。 |

**輸出(moveAssetReturn)**

IPS API不會傳回此作業的回應。

## 範例 {#section-78333769f4f14e2886fdf06433c9d2ad}

此程式碼範例會將資產移至資料夾。

**請求**

```java
<ns1:moveAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24266|1|17062</ns1:assetHandle>
   <ns1:folderHandle>MyCompany/My New Images/</ns1:folderHandle>
</ns1:moveAssetParam>
```

**回答**

無。
