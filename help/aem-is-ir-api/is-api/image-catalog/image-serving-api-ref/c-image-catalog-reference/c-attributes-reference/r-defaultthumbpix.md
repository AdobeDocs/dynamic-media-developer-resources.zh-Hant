---
description: 預設縮略圖大小。 用於縮略圖請求(req=tmb)，而不是屬性DefaultPix。
solution: Experience Manager
title: DefaultThumbPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c1413da0-a68d-4345-928f-b532991966a8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 2%

---

# DefaultThumbPix{#defaultthumbpix}

預設縮略圖大小。 用於縮略圖請求(req=tmb)，而不是屬性：:DefaultPix。

如果縮略圖請求( `req=tmb`)不顯式指定大小，而不顯式指定視圖大小 `wid=`。 `hei=`或 `scl=`。

## 屬性 {#section-650d9b1194fb4c47a03c6809e6b4af0e}

兩個整數，0或更大，用逗號分隔。 寬度和高度（以像素為單位）。 可以將其中一個或兩個值設定為0以保持它們不受約束。

不適用於嵌套/嵌入式請求。

## 預設 {#section-2c4a4f14540449638822913513170ff1}

繼承自 `default::DefaultThumbPix` 或為空。

## 另請參閱 {#section-4ad00963ffa049fcb17ad63e6bbe7ac4}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) 。 [黑=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)。 [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)。 [屬性：:DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
