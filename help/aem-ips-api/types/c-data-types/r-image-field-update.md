---
description: 更新與影像資產相關聯的影像欄位。
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 82bc016b-8a2b-4811-a0b4-1e2a93add3b6
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 9%

---

# ImageFieldUpdate{#imagefieldupdate}

更新與影像資產相關聯的影像欄位。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 資產控制代碼。 |
| `*`解析度`*` | `xsd:double` | 影像解析度（像素/英吋）。 |
| `*`anchorX`*` | `xsd:int` | X軸影像錨點。 |
| `*`anchorY`*` | `xsd:int` | Y軸影像錨點。 |
| `*`使用者資料`*` | `xsd:string` | `userData`中繼資料欄位的值，會發佈至提供使用者資料目錄欄位的影像。 |
