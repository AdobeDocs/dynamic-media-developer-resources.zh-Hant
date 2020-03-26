---
description: batchSetAssetMetadata操作中的新增更新的警告或錯誤詳細資料。
seo-description: batchSetAssetMetadata操作中的新增更新的警告或錯誤詳細資料。
seo-title: SetMetadataFault
solution: Experience Manager
title: SetMetadataFault
topic: Scene7 Image Production System API
uuid: 22302bb0-914a-4d50-a188-9c3ee58e0481
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SetMetadataFault{#setmetadatafault}

batchSetAssetMetadata操作中的新增更新的警告或錯誤詳細資料。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | 未成功設定中繼資料的資產。 |
| ` *`fieldHandle`*` | `xsd:string` | 設定其值未成功的中繼資料欄位的控制代碼。 |
| ` *`代碼`*` | `xsd:int` | 錯誤代碼。 |
| ` *`原因`*` | `xsd:string` | 故障描述（純文字檔案）。 |

