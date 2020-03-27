---
description: 目錄比對選項。
seo-description: 目錄比對選項。
seo-title: FullMatch
solution: Experience Manager
title: FullMatch
topic: Scene7 Image Serving - Image Rendering API
uuid: 0c69ba92-1411-4cb7-ac28-d26fe035222f
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# FullMatch{#fullmatch}

目錄比對選項。

目錄項在HTTP請求中指 ` *``*/ *`定為rootImageId`*` 對。 在剖析時，如果 ` *`rootId與目錄值相符`*` ，則會選取目錄，並且目錄記錄是透過將 `attribute::RootId` imageId與值相符來識 ` *``*``catalog::Id` 別。 如果找到目錄，但沒有與imageId匹配的目 ` *`錄條目`*`，則伺服器可以執行下列兩項操作之一：

如果 `attribute::FullMatch` 未設定，則伺服器使用匹配目錄的屬性。 在此例中， ` *`rootId會`*` 由 `attribute::RootPath` (若未在此目錄中 `default::RootPath`指定，則會取代)。

如果 `attribute::FullMatch` 已設定，伺服器將完全忽略目錄（如果未匹配目錄），然後使用預設目錄屬性繼續。 在這種情況下， ` *`rootId`*` 仍然是路徑的一部分(其前置 `default::RootPath`)。

## 屬性 {#section-25e021dbe6574d00aadd08a7fa0b6e81}

標幟. 設為0代表預設行為，或設為1以啟用完全符合行為。

## 預設 {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

繼承自 `default::FullMatch` （如果未定義或為空）。

## 另請參閱 {#section-42da0ba53e0b4c089c62108785faf5a9}

[屬性：:RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) , [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
