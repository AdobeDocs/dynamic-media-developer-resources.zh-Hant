---
description: 銳利化影像。 在進行所有縮放後，如果layer=comp，請將基本銳利化濾鏡套用至圖層或最終檢視影像。
solution: Experience Manager
title: op_sharpen
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 7%

---


# op_sharpen{#op-sharpen}

銳利化影像。 在進行所有縮放後，如果layer=comp，請將基本銳利化濾鏡套用至圖層或最終檢視影像。

`op_sharpen=0|1`

圖層遮色片或複合遮色片也會銳利化。

## 屬性 {#section-b27f3f6a27c34233b3f76805e18b2aa7}

層屬性或視圖屬性。 如果`layer=comp`，則套用至目前圖層或最終檢視影像。 被效果圖層忽略。

## 預設 {#section-665709700fff458e9dbbf8a78e8ecf71}

`op_sharpen=0`，以避免銳利化效果。

## 範例 {#section-3202122df5db4e14b358ecabfb6d8b85}

補償因影像重新取樣而造成的輕微模糊性。 我們也會提高JPEG品質，以避免沿著銳利邊緣產生額外的JPEG偽影。

`http://server/myRootId/myImageId?qlt=90,1&op_sharpen=1&wid=500`

## 另請參閱 {#section-d659199fde0d4c9dadebf1f09802915d}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_usm=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541)
