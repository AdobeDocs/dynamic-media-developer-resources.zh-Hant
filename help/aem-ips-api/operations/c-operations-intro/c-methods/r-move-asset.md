---
description: 將資產移至特定資料夾。
solution: Experience Manager
title: moveAsset
feature: Dynamic Media Classic,SDK/API，資產管理
role: Developer,Administrator
exl-id: c5357c1a-92ac-4f9c-957e-b62cb812796c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 15%

---

# moveAsset{#moveasset}

將資產移至特定資料夾。

語法

## 授權的使用者類型 {#section-e4f2d2a58132450aa36da6377134211e}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 為公司處理。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 處理您要移動的資產。 |
| `*`folderHandle`*` | `xsd:string` | 是 | 處理目標資料夾。 |

**輸出(moveAssetReturn)**

IPS API不會針對此操作傳回回應。

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
