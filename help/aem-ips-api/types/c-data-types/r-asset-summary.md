---
title: 資產摘要
description: 包含資產相關摘要資訊的中繼資料搜尋結果。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 25f16a2b-6cd8-485f-a6bd-2a9bc9b3243b
TQID: 'https://experienceleague.adobe.com/RHT8NJiS0pGKUcrYGBsSI1vewvRGUCZmsPYP6Pb0OBs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 10%

---

# [!DNL AssetSummary]{#assetsummary}

包含資產相關摘要資訊的中繼資料搜尋結果。

語法

## 參數 {#section-ebc75cc024d94c439260d2e71873cc74}

| 名稱 | 類型 | 說明 |
|---|---|---|
| assetHandle | `xsd:string` | 資產控制代碼。 |
| type | `xsd:string` | 資產型別。 「資產型別」常數會定義可能的值。 選擇性. |
| name | `xsd:string` | 資產名稱。 選擇性. |
| 資料夾 | `xsd:string` | 包含資產的資料夾。 |
| 檔案名 | `xsd:string` | 資產的檔案名稱。 |
| 已建立 | `xsd:dateTime` | 資產建立日期。 |
| createUser | `xsd:string` | 建立資產的使用者。 |
| lastModified | `xsd:dateTime` | 上次更新資產的日期。 |
| lastModifyUser | `xsd:string` | 上次修改資產的使用者。 |
| metadataArray | `types:MetadataArray` | 與資產相關聯的中繼資料值陣列。 |
| 分數 | `xsd:double` | 定義相似性搜尋的精確度（0 =沒有相符專案，1 =完全相符）。 |
| scoreDetail | `xsd:string` | 它儲存相似搜尋結果中類似區域的詳細資訊。 |

