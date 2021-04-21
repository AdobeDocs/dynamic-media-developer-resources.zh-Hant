---
description: 目錄比對選項。
solution: Experience Manager
title: FullMatch
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 3%

---


# FullMatch{#fullmatch}

目錄比對選項。

在HTTP請求中，目錄項指定為`*`rootId`*/ *`imageId`*`對。 在解析時，如果`*`rootId`*`與目錄的`attribute::RootId`值匹配，則選擇目錄，並且通過將`*`imageId`*`與`catalog::Id`值匹配來標識目錄記錄。 如果找到目錄，但沒有與`*`imageId`*`匹配的目錄條目，則伺服器可以執行下列兩項操作之一：

如果未設定`attribute::FullMatch`，則伺服器使用匹配目錄的屬性。 在這種情況下，`*`rootId`*`會由`attribute::RootPath`（或`default::RootPath`，若未在此目錄中指定）取代。

如果設定`attribute::FullMatch`，則伺服器會完全忽略目錄（如果未匹配目錄），然後使用預設目錄屬性繼續。 在此情況下，`*`rootId`*`仍為路徑的一部分（由`default::RootPath`前置）。

## 屬性 {#section-25e021dbe6574d00aadd08a7fa0b6e81}

標幟. 設為0代表預設行為，或設為1以啟用完全符合行為。

## 預設 {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

如果未定義或為空，則繼承自`default::FullMatch`。

## 另請參閱 {#section-42da0ba53e0b4c089c62108785faf5a9}

[屬性：:RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) , [目錄：Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
