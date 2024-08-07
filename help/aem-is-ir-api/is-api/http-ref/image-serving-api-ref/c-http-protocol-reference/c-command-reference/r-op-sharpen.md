---
title: op_sharpen
description: 銳利化影像。 如果圖層=comp，則在全部縮放之後，將基本銳利化濾鏡套用至圖層或最終檢視影像。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 62e7d91c-935f-410f-a971-ffb3cfff31d6
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

---

# op_sharpen{#op-sharpen}

銳利化影像。 如果圖層=comp，則在全部縮放之後，將基本銳利化濾鏡套用至圖層或最終檢視影像。

`op_sharpen=0|1`

圖層遮色片或複合遮色片也會銳利化。

## 屬性 {#section-b27f3f6a27c34233b3f76805e18b2aa7}

圖層屬性或檢視屬性。 套用至目前圖層或最終檢視影像（若為`layer=comp`）。 被效果圖層忽略。

## 預設 {#section-665709700fff458e9dbbf8a78e8ecf71}

`op_sharpen=0`，沒有銳利化效果。

## 範例 {#section-3202122df5db4e14b358ecabfb6d8b85}

補償影像重新取樣所導致的輕微模糊。 我們也會提高JPEG品質，以避免銳利化的邊緣產生額外的JPEG不自然感。

`http://server/myRootId/myImageId?qlt=90,1&op_sharpen=1&wid=500`

## 另請參閱 {#section-d659199fde0d4c9dadebf1f09802915d}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ， [op_usm=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541)
