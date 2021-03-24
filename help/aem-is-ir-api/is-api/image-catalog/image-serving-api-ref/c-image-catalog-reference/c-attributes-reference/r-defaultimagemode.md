---
description: 預設影像模式。 選擇在找不到請求中指定的影像時套用預設影像的方式。
solution: Experience Manager
title: DefaultImageMode
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

---


# DefaultImageMode{#defaultimagemode}

預設影像模式。 選擇在找不到請求中指定的影像時套用預設影像的方式。

## 屬性 {#section-7fa8acb63540490d9f5186231b5e77c3}

列舉。 &#39;0&#39;取代整張合成影像，即使遺失的影像只是數個圖層中的一個；&#39;1&#39;，以將每個遺失的圖層來源影像取代為預設影像，並照常傳回合成影像。

## 限制{#section-04cb0d50e8914564a8d226d0d4663c8b}

當巢狀影像演算、FXG或`req=set`請求失敗時，影像伺服會回復為`DefaultImageMode=0`。

## 預設 {#section-9e318524a2a5496386901286748c7ee7}

如果未定義或為空，則繼承自`default::DefaultImage`。

## 另請參閱 {#section-fddce1d27a0c43fb8b4d891f76ac5a52}

[defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433) ,  [attribute::DefaultImage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
