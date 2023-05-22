---
title: IccRenderIntent
description: 顏色轉換呈現意圖。 在未使用icc=指定渲染意圖時提供顏色轉換的預設渲染意圖。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86cc907d-556c-40ec-a104-2f0dcf9ed1ce
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 3%

---

# IccRenderIntent{#iccrenderintent}

顏色轉換呈現意圖。 在未指定渲染意圖時提供顏色轉換的預設渲染意圖 `icc=`。

## 屬性 {#section-0a38c60e1525426185616c42824aee2c}

枚舉。 設定為0表示感知，1表示相對比色，2表示飽和度，3表示絕對比色。 保留空值或設定為任何其它值，以使用顏色配置檔案中定義的預設渲染方法。

## 預設 {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

繼承自 `default::IccRenderIntent`的子菜單。 如果為空，則應用「相對比色」。

## 另請參閱 {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[屬性：:IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) 。 [屬性：:IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)。 [icc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
