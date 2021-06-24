---
description: 包含資產摘要資訊的中繼資料搜尋結果。
solution: Experience Manager
title: 資產摘要
feature: Dynamic Media Classic,SDK/API，資產管理
role: Developer,Administrator
exl-id: 25f16a2b-6cd8-485f-a6bd-2a9bc9b3243b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 10%

---

# 資產摘要{#assetsummary}

包含資產摘要資訊的中繼資料搜尋結果。

語法

## 參數 {#section-ebc75cc024d94c439260d2e71873cc74}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 資產控制代碼。 |
| `*`類型`*` | `xsd:string` | 資產類型. 「資產類型」常數會定義可能的值。 選填。 |
| `*`名稱`*` | `xsd:string` | 資產名稱。 選填。 |
| `*`資料夾`*` | `xsd:string` | 包含資產的資料夾。 |
| `*`檔案名`*` | `xsd:string` | 資產的檔案名。 |
| `*`created`*` | `xsd:dateTime` | 資產建立日期。 |
| `*`createUser`*` | `xsd:string` | 建立資產的使用者。 |
| `*`lastModified`*` | `xsd:dateTime` | 上次更新資產的日期。 |
| `*`lastModifyUser`*` | `xsd:string` | 修改資產的最後一個使用者。 |
| `*`metadataArray`*` | `types:MetadataArray` | 與資產相關聯的中繼資料值陣列。 |
| `*`分數`*` | `xsd:double` | 定義相似性搜尋時的精準度（0 =無相符，1 =完全相符）。 |
| `*`scoreDetail`*` | `xsd:string` | 包含相似性搜尋結果之類似區域的詳細資訊。 |
