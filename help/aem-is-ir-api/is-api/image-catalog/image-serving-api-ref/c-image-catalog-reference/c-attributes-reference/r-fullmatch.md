---
description: 目錄比對選項。
solution: Experience Manager
title: FullMatch
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 1a267c48-a8eb-426a-a70a-bdb9f5f20efb
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 3%

---

# FullMatch{#fullmatch}

目錄比對選項。

目錄項目在HTTP要求中指定為`*`rootId`*/ *`imageId`*`配對。 解析時，如果`*`rootId`*`匹配目錄的`attribute::RootId`值，則選擇目錄，並通過將`*`imageId`*`與`catalog::Id`值匹配來標識目錄記錄。 如果找到目錄，但沒有與`*`imageId`*`匹配的目錄項，則伺服器可以執行以下兩項之一：

如果未設定`attribute::FullMatch`，則伺服器使用匹配目錄的屬性。 在此情況下，`*`rootId`*`會由`attribute::RootPath`（若未在此目錄中指定，則為`default::RootPath`）取代。

如果設定了`attribute::FullMatch`，則伺服器會完全忽略目錄，就像沒有匹配任何目錄一樣，然後使用預設目錄屬性繼續操作。 在此情況下，`*`rootId`*`仍是路徑的一部分（由`default::RootPath`前置）。

## 屬性 {#section-25e021dbe6574d00aadd08a7fa0b6e81}

標幟. 預設行為設為0，或設為1以啟用完全符合行為。

## 預設 {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

如果未定義或為空，則從`default::FullMatch`繼承。

## 另請參閱 {#section-42da0ba53e0b4c089c62108785faf5a9}

[屬性：:RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) ,  [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
