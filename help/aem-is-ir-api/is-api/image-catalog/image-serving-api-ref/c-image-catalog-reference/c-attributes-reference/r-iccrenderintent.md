---
description: 色彩轉換演算目的。 當未使用icc=指定演算目的時，提供顏色轉換的預設演算目的。
solution: Experience Manager
title: IccRenderIntent
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 732b1935-6556-4420-a056-4e00cb3ed152
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 5%

---

# IccRenderIntent{#iccrenderintent}

色彩轉換演算目的。 當未使用icc=指定演算目的時，提供顏色轉換的預設演算目的。

## 屬性 {#section-2540099fb2fc47d29b04642da4f5922a}

列舉。 對於感知，設為0；對於相對比色，設為1；對於飽和度，設為2；對於絕對比色，設為3。

## 預設 {#section-61a05067905b44099c228e15de279dbd}

如果未定義或為空，則從`default::IccRenderIntent`繼承。

## 另請參閱 {#section-7da9ff3038ca452a9f7375a1ca0581af}

[attribute::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) *, [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f),  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)
