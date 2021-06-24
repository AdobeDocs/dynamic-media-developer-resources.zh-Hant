---
description: 預設JPEG編碼屬性。 指定JPEG回復影像的預設屬性。
solution: Experience Manager
title: JpegQuality
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: c2a7f7f9-0c2c-4421-9dbc-d5c1e936f0f1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 4%

---

# JpegQuality{#jpegquality}

預設JPEG編碼屬性。 指定JPEG回復影像的預設屬性。

## 屬性 {#section-7a75ebaf11bd4b778d287c2c5c150d0c}

整數和標幟，以逗號分隔。 第一個值在1..100範圍內，並定義品質。 對於正常行為，第二個值可以是0，或者禁用通常由JPEG編碼器使用的RGB色度下採樣。

## 預設 {#section-0b25eddd59bc434abfe38eeea9d45df3}

如果未定義或為空，則從`default::JpegQuality`繼承。

## 另請參閱 {#section-aa994afc02ea4f799655233ea32d36c9}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352)
