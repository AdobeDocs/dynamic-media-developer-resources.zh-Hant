---
description: PostScript檔案屬性。
seo-description: PostScript檔案屬性。
seo-title: GenerationInfo
solution: Experience Manager
title: GenerationInfo
topic: Dynamic Media Image Production System API
uuid: 166637e5-b981-4f64-8d92-5fce4f1b20d2
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 13%

---


# GenerationInfo{#generationinfo}

PostScript檔案屬性。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`引擎`*` | `xsd:string` | 使用的產生引擎（如需值，請參閱「產生資訊」）。 |
| `*`oribator`*` | `types:Asset` | 在生成中使用的主要資產的資產記錄。 |
| `*`已產生`*` | `types:Asset` | 產生的資產的資產記錄。 |
| `*`attributeArray`*` | `types:GenerationAttributeArray` | 與生成過程關聯的屬性陣列。 |

