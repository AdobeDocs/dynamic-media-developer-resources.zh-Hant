---
description: 相對影像URL的根URL。 指定相對影像URL的根URL。
seo-description: 相對影像URL的根URL。 指定相對影像URL的根URL。
seo-title: RootUrl
solution: Experience Manager
title: RootUrl
topic: Scene7 Image Serving - Image Rendering API
uuid: 173ce99a-f87e-4700-a28a-1a87b8c55b85
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---


# RootUrl{#rooturl}

相對影像URL的根URL。 指定相對影像URL的根URL。

`attribute::RootUrl` 使用，而非 `attribute::RootPath` 使用{ `src=` 大括 `mask=` 號}或（括弧）括住或值。

## 屬性 {#section-fe02269b4b724319a5d1f2cfcae31cba}

文字字串值。 絕對URL根路徑，包括前導通訊協定識別碼。 支援下列通訊協定：HTTP、HTTPS和FTP。

## 預設 {#section-fa5e3fc993c04086bc2b06dfeea4ae5c}

如果未定義，則繼承自`default::RootUrl`。 如果已定義但為空，則此影像目錄不支援相對URL。

## 另請參閱 {#section-ade4789086df4e76ae041cd4acfa2f85}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [attribute:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), ruleset:: [PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)
