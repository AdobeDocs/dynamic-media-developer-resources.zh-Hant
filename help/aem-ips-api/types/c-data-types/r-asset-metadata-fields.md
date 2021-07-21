---
description: 傳回指定資產類型的中繼資料欄位定義。
solution: Experience Manager
title: AssetMetadataFields
feature: Dynamic Media Classic, SDK/API，中繼資料，資產管理
role: Developer,Admin
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 8%

---

# AssetMetadataFields{#assetmetadatafields}

傳回指定資產類型的中繼資料欄位定義。

語法

## 參數 {#section-5ad771540c5f40c187b35e34aac19305}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`assetType`*` | `xsd:string` | 與欄位定義相關聯的資產類型（如需值，請參閱「資產類型」）。 |
| `*`fieldArray`*` | `types:MetadataFieldArray` | 與`assetType`中指定的資產類型相關聯的中繼資料欄位定義陣列。 |
