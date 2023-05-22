---
description: PDF檔案選項。
solution: Experience Manager
title: PDFOption
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 10%

---

# [!DNL PDFOptions]{#pdfoptions}

PDF檔案選項。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| 過程 | `xsd:string` | 選擇「PDF進程」。 |
| 解析度 | `xsd:double` | 檔案解析。 |
| 彩色空間 | `xsd:string` | 指令碼後顏色空間模式選項。 |
| pdf目錄 | `xsd:boolean` | 是否在呈現後將多頁PDF組合到eCatalog（預設值為true）。 |
| 抽取搜索詞 | `xsd:boolean` | 是否從PDF檔案提取搜索詞。 |
| 抽取連結 | `xsd:boolean` | 是否將PDF連結提取到IPS中分配給柵格化頁面的影像映射中。 |
