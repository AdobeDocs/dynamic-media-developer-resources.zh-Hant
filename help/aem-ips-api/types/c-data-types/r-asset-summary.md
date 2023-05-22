---
description: 包含有關資產的摘要資訊的元資料搜索結果。
solution: Experience Manager
title: 資產匯總
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 25f16a2b-6cd8-485f-a6bd-2a9bc9b3243b
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 12%

---

# [!DNL AssetSummary]{#assetsummary}

包含有關資產的摘要資訊的元資料搜索結果。

語法

## 參數 {#section-ebc75cc024d94c439260d2e71873cc74}

| 名稱 | 類型 | 說明 |
|---|---|---|
| 資產句柄 | `xsd:string` | 資產句柄。 |
| type | `xsd:string` | 資產類型. 「資產類型」常數定義可能的值。 選擇性. |
| name | `xsd:string` | 資產名稱。 選擇性. |
| 資料夾 | `xsd:string` | 包含資產的資料夾。 |
| 檔案名 | `xsd:string` | 資產的檔案名。 |
| 已建立 | `xsd:dateTime` | 資產建立日期。 |
| 建立用戶 | `xsd:string` | 建立資產的用戶。 |
| 上次修改時間 | `xsd:dateTime` | 上次更新資產的日期。 |
| 上次修改用戶 | `xsd:string` | 上次修改資產的用戶。 |
| 元資料陣列 | `types:MetadataArray` | 與資產關聯的元資料值的陣列。 |
| 分數 | `xsd:double` | 定義相似性搜索（0 =無匹配，1 =完全匹配）時的精度。 |
| 分數詳細資訊 | `xsd:string` | 保存作為相似性搜索結果的類似區域的詳細資訊。 |
