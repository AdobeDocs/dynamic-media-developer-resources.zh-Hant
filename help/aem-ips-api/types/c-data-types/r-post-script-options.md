---
description: PostScript檔案選項。
solution: Experience Manager
title: PostScript選項
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 13%

---

# PostScript選項{#postscriptoptions}

PostScript檔案選項。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| 過程 | `xsd:string` | PostScript進程選項。 |
| 解析度 | `xsd:double` | 檔案解析。 |
| 色域 | `xsd:string` | PostScript顏色空間模式。 |
| alpha | `xsd:boolean` | 是否將檔案柵格化為影像。 如果是，則如果以此方式定義原始檔案，則會建立透明背景。 通常用於建立重疊徽標。 |
| 抽取搜索詞 | `xsd:boolean` | 是否從PostScript檔案中提取搜索詞。 |
