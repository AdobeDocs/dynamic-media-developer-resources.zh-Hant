---
description: 預設JPEG編碼屬性。 指定JPEG回覆影像的預設屬性。
solution: Experience Manager
title: Jpeg品質
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2a7f7f9-0c2c-4421-9dbc-d5c1e936f0f1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 3%

---

# Jpeg品質{#jpegquality}

預設JPEG編碼屬性。 指定JPEG回覆影像的預設屬性。

## 屬性 {#section-7a75ebaf11bd4b778d287c2c5c150d0c}

整數與標幟，以逗號分隔。 第一個值在1到100的範圍內，並定義品質。 對於正常行為，第二個值可以是0；若要停用JPEG編碼器通常採用的RGB色度縮減取樣，可以是1。

## 預設 {#section-0b25eddd59bc434abfe38eeea9d45df3}

如果未定義或空白，則繼承自`default::JpegQuality`。

## 另請參閱 {#section-aa994afc02ea4f799655233ea32d36c9}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352)
