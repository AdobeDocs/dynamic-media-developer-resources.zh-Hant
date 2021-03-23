---
description: 傳回指定資產類型的中繼資料欄位定義。
seo-description: 傳回指定資產類型的中繼資料欄位定義。
seo-title: AssetMetadataFields
solution: Experience Manager
title: AssetMetadataFields
uuid: aefb734c-7609-4227-ae2c-48a1469740ec
feature: Dynamic Media經典，SDK/API，元資料，資產管理
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 7%

---


# AssetMetadataFields{#assetmetadatafields}

傳回指定資產類型的中繼資料欄位定義。

語法

## 參數 {#section-5ad771540c5f40c187b35e34aac19305}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`assetType`*` | `xsd:string` | 與欄位定義關聯的資產類型（如需值，請參閱「資產類型」）。 |
| `*`fieldArray`*` | `types:MetadataFieldArray` | 與`assetType`中指定的資產類型相關聯的中繼資料欄位定義陣列。 |

