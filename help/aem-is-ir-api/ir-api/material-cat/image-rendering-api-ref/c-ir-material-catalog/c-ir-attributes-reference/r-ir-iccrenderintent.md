---
title: IccRenderIntent
description: 色彩轉換演算色彩比對方式。 若未以「icc=」指定色彩演算比對方式，則它提供預設的色彩演算比對方式供色彩轉換使用。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86cc907d-556c-40ec-a104-2f0dcf9ed1ce
TQID: 'https://experienceleague.adobe.com/5BehWh36v-kv7Z8kSj-WwoqBgyk4TC8srAhxKs89mnE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 101
ht-degree: 2%

---

# IccRenderIntent{#iccrenderintent}

色彩轉換演算色彩比對方式。 提供未以`icc=`指定色彩轉換時的預設色彩演算比對方式。

## 屬性 {#section-0a38c60e1525426185616c42824aee2c}

列舉。 設為0代表可感知，1代表相對比色，2代表飽和度，3代表絕對比色。 請保持空白或設定為任何其他值，以便使用顏色設定檔中定義的預設色彩演算比對方式。

## 預設 {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

如果未定義，則繼承自`default::IccRenderIntent`。 如果空白，會套用「相對比色」。

## 另請參閱 {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[attribute：：IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) ， [attribute：：IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)， [`icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)

