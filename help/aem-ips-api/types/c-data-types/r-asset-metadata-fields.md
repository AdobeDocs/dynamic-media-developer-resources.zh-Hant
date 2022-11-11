---
title: AssetMetadataFields
description: 傳回指定資產類型的中繼資料欄位定義。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 10%

---

# [!DNL AssetMetadataFields]{#assetmetadatafields}

傳回指定資產類型的中繼資料欄位定義。

語法

## 參數 {#section-5ad771540c5f40c187b35e34aac19305}

| 名稱 | 類型 | 說明 |
|---|---|---|
| assetType | `xsd:string` | 與欄位定義相關聯的資產類型（如需值，請參閱「資產類型」）。 |
| fieldArray | `types:MetadataFieldArray` | 與中指定的資產類型相關聯的中繼資料欄位定義陣列， `assetType`. |
