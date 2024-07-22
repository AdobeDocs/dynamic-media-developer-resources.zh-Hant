---
description: PostScript檔案選項。
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '65'
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
