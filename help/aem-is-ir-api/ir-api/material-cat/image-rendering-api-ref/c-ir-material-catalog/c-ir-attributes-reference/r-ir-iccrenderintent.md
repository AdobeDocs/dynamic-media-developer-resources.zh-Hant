---
description: 色彩轉換演算目的。 當未使用icc=指定演算目的時，提供顏色轉換的預設演算目的。
solution: Experience Manager
title: IccRenderIntent
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86cc907d-556c-40ec-a104-2f0dcf9ed1ce
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---

# IccRenderIntent{#iccrenderintent}

色彩轉換演算目的。 當未使用icc=指定演算目的時，提供顏色轉換的預設演算目的。

## 屬性 {#section-0a38c60e1525426185616c42824aee2c}

列舉。 對於感知，設為0；對於相對比色，設為1；對於飽和度，設為2；對於絕對比色，設為3。 保留空白或設為任何其他值，以使用顏色設定檔中定義的預設演算方式。

## 預設 {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

如果未定義，則繼承自`default::IccRenderIntent`。 如果為空，則應用「相對比色」。

## 另請參閱 {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[屬性：:IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) ，屬 [性：:IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0),  [icc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
