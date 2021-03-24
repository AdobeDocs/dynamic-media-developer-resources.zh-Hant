---
description: batchSetAssetMetadata操作中的新增更新的警告或錯誤詳細資料。
solution: Experience Manager
title: SetMetadataFault
feature: Dynamic Media經典，SDK/API，中繼資料
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 10%

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

