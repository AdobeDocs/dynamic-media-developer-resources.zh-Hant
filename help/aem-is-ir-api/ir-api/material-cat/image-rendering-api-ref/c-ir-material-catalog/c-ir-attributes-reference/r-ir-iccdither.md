---
title: Icc遞色
description: 色彩轉換遞色。 指定在沒有icc=明確選取時，是否應使用遞色來改善色彩轉換的感應品質。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bb1bec31-3f7c-48c8-9456-6359b739a657
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 3%

---

# Icc遞色{#iccdither}

色彩轉換遞色。 指定當未使用`icc=`進行明確選取時，是否應使用遞色來改善色彩轉換的感應品質。

## 屬性 {#section-646fb48084734c66bf648360f3a5bfd1}

標幟。 設定為`0`以停用或設定為`1`以啟用遞色。

## 預設 {#section-c9066c361215404d847f4d2c8f1ea3a5}

如果未定義或空白，則繼承自`default::IccDither`。

## 另請參閱 {#section-76a376a1bee74670867b4de81fea65aa}

[attribute：：IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) ， [icc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
