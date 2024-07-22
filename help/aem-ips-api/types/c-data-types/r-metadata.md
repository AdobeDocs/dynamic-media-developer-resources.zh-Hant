---
description: searchAssets傳回的中繼資料欄位。
solution: Experience Manager
title: 中繼資料
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 62e3e215-31ea-49fd-937e-d136fdf84aff
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 14%

---

# [!DNL Metadata]{#metadata}

searchAssets傳回的中繼資料欄位。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名稱 | 類型 | 說明 |
|---|---|---|
| name | `xsd:string` | 中繼資料名稱。 |
| 價值 | `xsd:string` | 中繼資料值。 |
| boolVal | `xsd:boolean` | 布林值中繼資料值（僅適用於布林型別欄位）。 |
| longVal | `xsd:long` | 長中繼資料值（僅適用於int型別的欄位）。 |
| doubleVal | `xsd:double` | 雙倍中繼資料值（僅適用於浮點型欄位）。 |
| 日期值 | `xsd:dateTime` | 日期中繼資料值（僅適用於日期型別欄位）。 |
