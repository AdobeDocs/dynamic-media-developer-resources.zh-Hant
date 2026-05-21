---
description: PostScript檔案屬性。
solution: Experience Manager
title: GenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9aac2973-bbcb-4914-9bf9-203f0357527c
TQID: 'https://experienceleague.adobe.com/fM-heKQFWRXUn8QWVxJA1yNJ2aqlozRoK5B-ErzamLA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 45
ht-degree: 11%

---

# [!DNL GenerationInfo]{#generationinfo}

PostScript檔案屬性。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| [!DNL engine] | `xsd:string` | 使用的產生引擎（請參閱「產生資訊」以瞭解值）。 |
| [!DNL originator] | `types:Asset` | 產生中使用的主要資產的資產記錄。 |
| [!DNL generated] | `types:Asset` | 產生的資產的資產記錄。 |
| attributearray | `types:GenerationAttributeArray` | 與產生程式相關聯的屬性陣列。 |
