---
title: IccRenderIntent
description: 色彩轉換演算色彩比對方式。 如果未針對演算色彩比對方式指定「icc=」，則它提供色彩轉換的預設色彩比對方式。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 732b1935-6556-4420-a056-4e00cb3ed152
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 4%

---

# IccRenderIntent{#iccrenderintent}

色彩轉換演算色彩比對方式。 提供色彩轉換的預設色彩演算比對方式（若未指定色彩演算比對方式）。 `icc=`.

## 屬性 {#section-2540099fb2fc47d29b04642da4f5922a}

列舉。 設為0代表可感知，1代表相對比色，2代表飽和度，3代表絕對比色。

## 預設 {#section-61a05067905b44099c228e15de279dbd}

繼承自 `default::IccRenderIntent` 若未定義或為空。

## 另請參閱 {#section-7da9ff3038ca452a9f7375a1ca0581af}

[attribute：：IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) &#42;， [屬性：：IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f)， [`icc=`](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)
