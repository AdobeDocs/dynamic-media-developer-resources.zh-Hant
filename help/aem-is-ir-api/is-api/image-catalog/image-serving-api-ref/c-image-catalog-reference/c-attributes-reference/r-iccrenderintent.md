---
description: 色彩轉換演算方式。 在未使用icc=指定演算方式時，提供色彩轉換的預設演算方式。
solution: Experience Manager
title: IccRenderIntent
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 4%

---


# IccRenderIntent{#iccrenderintent}

色彩轉換演算方式。 在未使用icc=指定演算方式時，提供色彩轉換的預設演算方式。

## 屬性 {#section-2540099fb2fc47d29b04642da4f5922a}

列舉。 設為0表示感應色，1表示相對比色，2表示飽和度，3表示絕對比色。

## 預設 {#section-61a05067905b44099c228e15de279dbd}

如果未定義或為空，則繼承自`default::IccRenderIntent`。

## 另請參閱 {#section-7da9ff3038ca452a9f7375a1ca0581af}

[attribute::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) *,  [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)
