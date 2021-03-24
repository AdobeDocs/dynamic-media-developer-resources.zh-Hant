---
description: 色彩轉換演算方式。 在未使用icc=指定演算方式時，提供色彩轉換的預設演算方式。
solution: Experience Manager
title: IccRenderIntent
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 3%

---


# IccRenderIntent{#iccrenderintent}

色彩轉換演算方式。 在未使用icc=指定演算方式時，提供色彩轉換的預設演算方式。

## 屬性 {#section-0a38c60e1525426185616c42824aee2c}

列舉。 設為0表示感應色，1表示相對比色，2表示飽和度，3表示絕對比色。 保留空白或設定為任何其他值，以使用顏色配置檔案中定義的預設渲染方式。

## 預設 {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

繼承自`default::IccRenderIntent`（如果未定義）。 如果為空，則應用「相對比色」。

## 另請參閱 {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[attribute::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) ,  [attribute::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0), [icc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
