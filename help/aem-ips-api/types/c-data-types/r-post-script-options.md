---
description: PostScript檔案選項。
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
TQID: 'https://experienceleague.adobe.com/XsIiYor0c-7I34OYazNaSF0Hx3sbZmzpTzAT1u73xxo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 65
ht-degree: 12%

---

# [!DNL PostScriptOptions]{#postscriptoptions}

PostScript檔案選項。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| 過程 | `xsd:string` | PostScript程式選擇。 |
| 解析度 | `xsd:double` | 檔案解析度。 |
| 色域 | `xsd:string` | PostScript色域模式。 |
| alpha | `xsd:boolean` | 是否將檔案點陣化成影像。 如果是這樣的話，如果以這種方式定義原始檔案，則會建立透明背景。 通常用於建立重疊圖志。 |
| extractSearchWords | `xsd:boolean` | 是否要從PostScript檔案擷取搜尋字詞。 |
