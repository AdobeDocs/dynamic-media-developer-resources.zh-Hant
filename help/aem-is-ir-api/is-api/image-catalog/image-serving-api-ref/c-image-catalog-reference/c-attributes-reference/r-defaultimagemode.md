---
description: 預設影像模式。 在找不到請求中指定的影像時，選取如何套用預設影像。
solution: Experience Manager
title: DefaultImageMode
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: b30ce72f-7c74-407c-bd4a-042b84c469e9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---

# DefaultImageMode{#defaultimagemode}

預設影像模式。 在找不到請求中指定的影像時，選取如何套用預設影像。

## 屬性 {#section-7fa8acb63540490d9f5186231b5e77c3}

列舉。 「0」替換整個複合影像，即使丟失的影像只是多個圖層中的一個；「1」，用預設影像替換每個缺少的圖層源影像，並照常返回複合影像。

## 限制 {#section-04cb0d50e8914564a8d226d0d4663c8b}

巢狀影像呈現、FXG或`req=set`請求失敗時，影像提供會回復為`DefaultImageMode=0`。

## 預設 {#section-9e318524a2a5496386901286748c7ee7}

如果未定義或為空，則從`default::DefaultImage`繼承。

## 另請參閱 {#section-fddce1d27a0c43fb8b4d891f76ac5a52}

[defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433) ,  [attribute::DefaultImage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
