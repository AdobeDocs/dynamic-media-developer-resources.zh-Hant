---
title: 資產元資料欄位
description: 返回指定資產類型的元資料欄位定義。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 10%

---

# 資產元資料欄位{#assetmetadatafields}

返回指定資產類型的元資料欄位定義。

語法

## 參數 {#section-5ad771540c5f40c187b35e34aac19305}

| 名稱 | 類型 | 說明 |
|---|---|---|
| 資產類型 | `xsd:string` | 與欄位定義關聯的資產類型（有關值，請參閱「資產類型」）。 |
| 欄位陣列 | `types:MetadataFieldArray` | 與中指定的資產類型關聯的元資料欄位定義的陣列 `assetType`。 |
