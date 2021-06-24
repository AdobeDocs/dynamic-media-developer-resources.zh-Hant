---
description: PostScript檔案選項。
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 11%

---

# PostScriptOptions{#postscriptoptions}

PostScript檔案選項。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`過程`*` | `xsd:string` | PostScript程式選項。 |
| `*`解析度`*` | `xsd:double` | 檔案解析。 |
| `*`色域`*` | `xsd:string` | PostScript colorspace模式。 |
| `*`alpha`*` | `xsd:boolean` | 是否將檔案柵格化為影像。 如果是，如果以此方式定義原始檔案，則將建立透明背景。 通常用於建立覆蓋標誌。 |
| `*`extractSearchWords`*` | `xsd:boolean` | 是否從PostScript檔案中擷取搜尋字詞。 |
