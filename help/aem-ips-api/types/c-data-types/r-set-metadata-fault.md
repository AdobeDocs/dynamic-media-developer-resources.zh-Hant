---
description: batchSetAssetMetadata操作中新更新的警告或錯誤詳細資訊。
solution: Experience Manager
title: SetMetadataFault
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 49c6f355-4b5f-4b98-9a58-5732d56fdccb
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 12%

---

# SetMetadataFault{#setmetadatafault}

batchSetAssetMetadata操作中新更新的警告或錯誤詳細資訊。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| 資產句柄 | `xsd:string` | 元資料設定失敗的資產。 |
| 欄位句柄 | `xsd:string` | 設定其值失敗的元資料欄位的句柄。 |
| 代碼 | `xsd:int` | 錯誤代碼。 |
| 原因 | `xsd:string` | 故障描述（純文字檔案）。 |
