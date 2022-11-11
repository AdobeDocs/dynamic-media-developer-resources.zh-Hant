---
description: PDF檔案選項。
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 11%

---

# [!DNL PDFOptions]{#pdfoptions}

PDF檔案選項。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| 過程 | `xsd:string` | 選擇「PDF程式」。 |
| 解析度 | `xsd:double` | 檔案解析。 |
| 色域 | `xsd:string` | 指令碼後顏色空間模式選項。 |
| pdfCatalog | `xsd:boolean` | 轉譯後是否要將多個頁面PDF合併為eCatalog（預設為true）。 |
| extractSearchWords | `xsd:boolean` | 是否從PDF檔案中擷取搜尋字詞。 |
| extractLinks | `xsd:boolean` | 是否將PDF連結提取到指派給IPS內柵格化頁的影像映射中。 |
