---
description: 包含資產摘要資訊的中繼資料搜尋結果。
seo-description: 包含資產摘要資訊的中繼資料搜尋結果。
seo-title: 資產摘要
solution: Experience Manager
title: 資產摘要
topic: Scene7 Image Production System API
uuid: 0ac8f900-c16c-409d-b83c-3bdf0ad28fac
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 資產摘要{#assetsummary}

包含資產摘要資訊的中繼資料搜尋結果。

語法

## 參數 {#section-ebc75cc024d94c439260d2e71873cc74}

| 名稱 | 類型 | 說明 |
|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | 資產控制代碼。 |
| ` *`類型`*` | `xsd:string` | 資產類型. 「資產類型」常數會定義可能的值。 選填。 |
| ` *`名稱`*` | `xsd:string` | 資產名稱。 選填。 |
| ` *`資料夾`*` | `xsd:string` | 包含資產的資料夾。 |
| ` *`檔案名`*` | `xsd:string` | 資產的檔案名稱。 |
| ` *`created`*` | `xsd:dateTime` | 資產建立日期。 |
| ` *`createUser`*` | `xsd:string` | 建立資產的使用者。 |
| ` *`lastModified`*` | `xsd:dateTime` | 上次更新資產的日期。 |
| ` *`lastModifyUser`*` | `xsd:string` | 上次修改資產的使用者。 |
| ` *`metadataArray`*` | `types:MetadataArray` | 與資產相關聯的中繼資料值陣列。 |
| ` *`分數`*` | `xsd:double` | 定義相似性搜尋時的精確度（0 =無匹配，1 =完全匹配）。 |
| ` *`scoreDetail`*` | `xsd:string` | 保存由於相似性搜索而導致的類似區域的詳細資訊。 |

