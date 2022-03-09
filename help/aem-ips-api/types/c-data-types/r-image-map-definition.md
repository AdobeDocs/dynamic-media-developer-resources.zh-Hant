---
description: 瀏覽器中按一下操作的目標定義。
solution: Experience Manager
title: 影像映射定義
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 12%

---

# 影像映射定義{#imagemapdefinition}

瀏覽器中按一下操作的目標定義。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| 名稱 | `xsd:string` | 影像映射定義的名稱。 |
| 形狀類型 | `xsd:string` | 區域形狀值之一。 |
| 區域 | `xsd:string` | 影像地圖坐標。 格式基於HTML `<area>` 標籤屬性。 |
| 操作 | `xsd:string` | 要包括在HTML中的其他屬性 `<area>` 標籤，包括 `href` URL。 |
| 啟動 | `xsd:boolean` | 如果啟用了影像映射，則為True。 |
