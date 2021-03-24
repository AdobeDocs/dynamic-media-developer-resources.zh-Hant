---
description: 傳回指定資產類型的中繼資料欄位定義。
solution: Experience Manager
title: AssetMetadataFields
feature: Dynamic Media經典，SDK/API，元資料，資產管理
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 8%

---


# AssetMetadataFields{#assetmetadatafields}

傳回指定資產類型的中繼資料欄位定義。

語法

## 參數 {#section-5ad771540c5f40c187b35e34aac19305}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`assetType`*` | `xsd:string` | 與欄位定義關聯的資產類型（如需值，請參閱「資產類型」）。 |
| `*`fieldArray`*` | `types:MetadataFieldArray` | 與`assetType`中指定的資產類型相關聯的中繼資料欄位定義陣列。 |

