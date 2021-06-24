---
description: 作業日誌資訊。
solution: Experience Manager
title: 作業日誌詳細資訊
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: fe41a48a-4671-4179-a128-aadc7bc0683b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 7%

---

# 作業日誌詳細資訊{#joblogdetail}

作業日誌資訊。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`logMessage`*` | `xsd:string` | 作業日誌中的消息。 |
| `*`logType`*` | `xsd:string` | 作業日誌檔案類型。 |
| `*`assetName`*` | `xsd:string` | 作業記錄中的資產名稱（選用）。 |
| `*`assetType`*` | `xsd:string` | 選擇資產類型。 |
| `*`assetHandle`*` | `xsd:string` | 作業記錄中參考的資產處理代碼。 |
| `*`auxArray`*` | `types:JobLogDetailAuxArray` | 提供上述五種作業日誌類型以外的其他詳細作業日誌資訊。 |
