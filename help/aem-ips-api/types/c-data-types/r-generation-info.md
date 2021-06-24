---
description: PostScript檔案屬性。
solution: Experience Manager
title: GenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 9aac2973-bbcb-4914-9bf9-203f0357527c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 12%

---

# GenerationInfo{#generationinfo}

PostScript檔案屬性。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`引擎`*` | `xsd:string` | 使用的產生引擎（有關值，請參閱「產生資訊」）。 |
| `*`發件人`*` | `types:Asset` | 產生時使用的主要資產的資產記錄。 |
| `*`已產生`*` | `types:Asset` | 所產生資產的資產記錄。 |
| `*`attributeArray`*` | `types:GenerationAttributeArray` | 與生成過程相關聯的屬性陣列。 |
