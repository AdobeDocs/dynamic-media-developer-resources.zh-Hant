---
description: batchSetAssetMetadata操作中的新增更新的警告或錯誤詳細資料。
seo-description: batchSetAssetMetadata操作中的新增更新的警告或錯誤詳細資料。
seo-title: SetMetadataFault
solution: Experience Manager
title: SetMetadataFault
uuid: 22302bb0-914a-4d50-a188-9c3ee58e0481
feature: Dynamic Media經典，SDK/API，中繼資料
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 8%

---


# SetMetadataFault{#setmetadatafault}

batchSetAssetMetadata操作中的新增更新的警告或錯誤詳細資料。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 未成功設定中繼資料的資產。 |
| `*`fieldHandle`*` | `xsd:string` | 設定其值未成功的中繼資料欄位的控制代碼。 |
| `*`代碼`*` | `xsd:int` | 錯誤代碼。 |
| `*`原因`*` | `xsd:string` | 故障描述（純文字檔案）。 |

