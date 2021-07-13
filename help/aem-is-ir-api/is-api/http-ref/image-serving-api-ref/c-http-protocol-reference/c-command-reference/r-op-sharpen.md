---
description: 銳化影像。 如果layer=comp，則在所有縮放後，將基本銳利化濾鏡應用於圖層或最終視圖影像。
solution: Experience Manager
title: op_sharpen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 62e7d91c-935f-410f-a971-ffb3cfff31d6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 7%

---

# op_sharpen{#op-sharpen}

銳化影像。 如果layer=comp，則在所有縮放後，將基本銳利化濾鏡應用於圖層或最終視圖影像。

`op_sharpen=0|1`

圖層蒙版或複合蒙版也被銳化。

## 屬性 {#section-b27f3f6a27c34233b3f76805e18b2aa7}

層屬性或視圖屬性。 若`layer=comp`，則套用至目前層或最終檢視影像。 被效果層忽略。

## 預設 {#section-665709700fff458e9dbbf8a78e8ecf71}

`op_sharpen=0`，不會銳利化。

## 範例 {#section-3202122df5db4e14b358ecabfb6d8b85}

補償因影像重採樣而導致的輕微模糊性。 我們還提高了JPEG質量，以避免沿著銳化邊緣出現其他JPEG偽影。

`http://server/myRootId/myImageId?qlt=90,1&op_sharpen=1&wid=500`

## 另請參閱 {#section-d659199fde0d4c9dadebf1f09802915d}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_usm=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541)
