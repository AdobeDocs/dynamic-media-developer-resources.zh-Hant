---
description: 目錄匹配選項。
solution: Experience Manager
title: 完全匹配
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1a267c48-a8eb-426a-a70a-bdb9f5f20efb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 2%

---

# 完全匹配{#fullmatch}

目錄匹配選項。

將目錄條目指定為 `*`根ID`*/ *`影像ID`*` HTTP請求中的對。 分析時，如果 `*`根ID`*` 與 `attribute::RootId` 目錄的值，並且通過匹配來標識目錄記錄 `*`影像ID`*` 帶 `catalog::Id` 值。 如果找到目錄，但沒有匹配的目錄條目 `*`影像ID`*`，伺服器可以執行以下兩項之一：

如果 `attribute::FullMatch` 未設定，伺服器使用匹配目錄的屬性。 在這個例子中， `*`根ID`*` 替換為 `attribute::RootPath` 或 `default::RootPath`，如果未在此目錄中指定)。

如果 `attribute::FullMatch` 設定後，伺服器將完全忽略目錄，就像未匹配任何目錄一樣，並繼續使用預設目錄屬性。 在這個例子中， `*`根ID`*` 仍然是路徑的一部分(該路徑被 `default::RootPath`)。

## 屬性 {#section-25e021dbe6574d00aadd08a7fa0b6e81}

標幟. 將預設行為設定為0或將啟用完全匹配行為設定為1。

## 預設 {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

繼承自 `default::FullMatch` 或為空。

## 另請參閱 {#section-42da0ba53e0b4c089c62108785faf5a9}

[屬性：:RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) 。 [目錄：:ID](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
