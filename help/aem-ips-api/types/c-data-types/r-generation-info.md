---
description: PostScript檔案屬性。
solution: Experience Manager
title: 生成資訊
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9aac2973-bbcb-4914-9bf9-203f0357527c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 11%

---

# [!DNL GenerationInfo]{#generationinfo}

PostScript檔案屬性。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| [!DNL engine] | `xsd:string` | 使用的生成引擎（有關值，請參閱「生成資訊」）。 |
| [!DNL originator] | `types:Asset` | 生成中使用的主要資產的資產記錄。 |
| [!DNL generated] | `types:Asset` | 生成的資產的資產記錄。 |
| 屬性陣列 | `types:GenerationAttributeArray` | 與生成進程關聯的屬性陣列。 |
