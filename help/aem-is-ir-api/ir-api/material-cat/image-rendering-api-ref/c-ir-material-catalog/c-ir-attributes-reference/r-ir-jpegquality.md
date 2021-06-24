---
description: 預設JPEG編碼質量。 指定JPEG編碼回復影像的預設質量設定。
solution: Experience Manager
title: JpegQuality
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 1a699a9e-dbf6-4e01-95aa-37a6eb83f4df
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 4%

---

# JpegQuality{#jpegquality}

預設JPEG編碼質量。 指定JPEG編碼回復影像的預設質量設定。

## 屬性 {#section-8b1ed3e0acaa4fbfa050b74c00b9d4dc}

整數和標幟，以逗號分隔。 第一個值在1..100範圍內，並定義品質。 對於正常行為，第二個值可以是0，或者禁用通常由JPEG編碼器使用的色度下採樣。

## 預設 {#section-60900c0fb8c54444b2361513232514db}

如果未定義或為空，則從`default::JpegQuality`繼承。

## 另請參閱 {#section-8928a28fcbfe401cad4d4021a7a1c268}

[qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd)
