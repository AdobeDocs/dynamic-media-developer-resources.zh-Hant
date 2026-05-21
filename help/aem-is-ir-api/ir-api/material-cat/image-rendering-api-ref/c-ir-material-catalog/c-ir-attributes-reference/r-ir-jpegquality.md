---
title: Jpeg品質
description: 預設JPEG編碼品質。 指定JPEG編碼的回覆影像的預設品質設定。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1a699a9e-dbf6-4e01-95aa-37a6eb83f4df
TQID: 'https://experienceleague.adobe.com/h7SBTIJh-a1Z0e3hfMA5TSXDI3ft809TrWyCggl8loU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 83
ht-degree: 3%

---

# Jpeg品質{#jpegquality}

預設JPEG編碼品質。 指定JPEG編碼的回覆影像的預設品質設定。

## 屬性 {#section-8b1ed3e0acaa4fbfa050b74c00b9d4dc}

整數與標幟，以逗號分隔。 第一個值在1到100的範圍內，並定義品質。 第二個值可能是`0` （正常行為），或是`1` （停用JPEG編碼器採用的色度縮減取樣）。

## 預設 {#section-60900c0fb8c54444b2361513232514db}

如果未定義或空白，則繼承自`default::JpegQuality`。

## 另請參閱 {#section-8928a28fcbfe401cad4d4021a7a1c268}

[qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd)
