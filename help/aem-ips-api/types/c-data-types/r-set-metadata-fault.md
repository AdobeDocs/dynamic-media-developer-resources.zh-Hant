---
description: batchSetAssetMetadata操作中單一更新的警告或錯誤詳細資訊。
solution: Experience Manager
title: SetMetadataFault
feature: Dynamic Media Classic,SDK/API，中繼資料
role: Developer,Administrator
exl-id: 49c6f355-4b5f-4b98-9a58-5732d56fdccb
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 10%

---

# SetMetadataFault{#setmetadatafault}

batchSetAssetMetadata操作中單一更新的警告或錯誤詳細資訊。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 未成功設定中繼資料的資產。 |
| `*`fieldHandle`*` | `xsd:string` | 元資料欄位的句柄，其值未成功設定。 |
| `*`代碼`*` | `xsd:int` | 錯誤代碼。 |
| `*`原因`*` | `xsd:string` | 錯誤描述（純文字檔案）。 |
