---
description: PDF檔案選項。
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
TQID: 'https://experienceleague.adobe.com/gjd-g7jhWVbLRL3kYnkX96ihjkiK34oCp7Ns1iC89GM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 68
ht-degree: 10%

---

# [!DNL PDFOptions]{#pdfoptions}

PDF檔案選項。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| 過程 | `xsd:string` | 選擇「PDF程式」。 |
| 解析度 | `xsd:double` | 檔案解析度。 |
| 色域 | `xsd:string` | 後置指令碼色彩空間模式選擇。 |
| pdfCatalog | `xsd:boolean` | 轉譯後是否將多頁PDF結合至eCatalog （預設為true）。 |
| extractSearchWords | `xsd:boolean` | 是否要從PDF檔案擷取搜尋字詞。 |
| extractLinks | `xsd:boolean` | 是否要將PDF連結擷取至指派給IPS內點陣化頁面的影像地圖。 |

