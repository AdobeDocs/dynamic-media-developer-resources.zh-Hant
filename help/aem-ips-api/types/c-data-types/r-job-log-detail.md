---
description: 作業日誌資訊。
solution: Experience Manager
title: 作業日誌詳細資訊
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fe41a48a-4671-4179-a128-aadc7bc0683b
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 8%

---

# [!DNL JobLogDetail]{#joblogdetail}

作業日誌資訊。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| 日誌消息 | `xsd:string` | 作業日誌中的消息。 |
| 日誌類型 | `xsd:string` | 作業日誌檔案類型。 |
| 資產名稱 | `xsd:string` | 作業日誌中的資產名稱（可選）。 |
| 資產類型 | `xsd:string` | 資產類型的選擇。 |
| 資產句柄 | `xsd:string` | 作業日誌中引用的資產句柄。 |
| aux陣列 | `types:JobLogDetailAuxArray` | 提供上述五種作業日誌類型之外的其他詳細作業日誌資訊。 |
