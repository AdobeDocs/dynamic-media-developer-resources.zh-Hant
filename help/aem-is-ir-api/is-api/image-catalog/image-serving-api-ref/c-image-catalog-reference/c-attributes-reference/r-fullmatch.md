---
description: 目錄比對選項。
solution: Experience Manager
title: Fullmatch
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1a267c48-a8eb-426a-a70a-bdb9f5f20efb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 1%

---

# Fullmatch{#fullmatch}

目錄比對選項。

目錄專案在HTTP要求中指定為`*`rootId`*/ *`imageId`*`配對。 剖析時，如果`*`rootId`*`符合目錄的`attribute::RootId`值，則會選取目錄，而目錄記錄會透過將`*`imageId`*`與`catalog::Id`值比對來識別。 如果找到目錄，但沒有符合`*`imageId`*`的目錄專案，伺服器可以執行下列其中一項作業：

如果未設定`attribute::FullMatch`，伺服器會使用相符目錄的屬性。 在此案例中，`*`rootId`*`已由`attribute::RootPath`取代（如果未在此目錄中指定，則為`default::RootPath`）。

如果設定`attribute::FullMatch`，伺服器會完全忽略目錄（就像沒有相符的目錄一樣），然後繼續使用預設的目錄屬性。 在此情況下，`*`rootId`*`仍為路徑的一部分（前置為`default::RootPath`）。

## 屬性 {#section-25e021dbe6574d00aadd08a7fa0b6e81}

標幟。 將預設行為設定為0，或將設定為1以啟用完全相符行為。

## 預設 {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

如果未定義或空白，則繼承自`default::FullMatch`。

## 另請參閱 {#section-42da0ba53e0b4c089c62108785faf5a9}

[attribute：：RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) ， [catalog：：Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
