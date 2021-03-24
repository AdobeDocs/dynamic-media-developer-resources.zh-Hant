---
description: PDF檔案選項。
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 9%

---


# PDFOptions{#pdfoptions}

PDF檔案選項。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`過程`*` | `xsd:string` | 選擇「PDF流程」。 |
| `*`解析度`*` | `xsd:double` | 檔案解析度。 |
| `*`色域`*` | `xsd:string` | 指令碼後色域模式選項。 |
| `*`pdfCatalog`*` | `xsd:boolean` | 是否在轉譯後將多頁PDF合併為eCatalog（預設為true）。 |
| `*`extractSearchWords`*` | `xsd:boolean` | 是否從PDF檔案擷取搜尋字詞。 |
| `*`extractLinks`*` | `xsd:boolean` | 是否將PDF連結擷取至指派給IPS中點陣化頁面的影像地圖。 |

