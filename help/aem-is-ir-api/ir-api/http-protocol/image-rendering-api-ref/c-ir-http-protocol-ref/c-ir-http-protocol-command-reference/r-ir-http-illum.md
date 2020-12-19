---
description: 照明圖選擇器。 指定此材料希望用來渲染的照明映射。
seo-description: 照明圖選擇器。 指定此材料希望用來渲染的照明映射。
seo-title: illum
solution: Experience Manager
title: illum
topic: Scene7 Image Serving - Image Rendering API
uuid: 16c7144f-7f16-47d1-8140-fd679e702660
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# illum{#illum}

照明圖選擇器。 指定此材料希望用來渲染的照明映射。

`illum=-1|0|1|2`

如果指定的照明地圖在目標暈映中不可用，則改用最近的可用地圖。

`illum=-1` 指定照明映射是根據值自動選 `gloss=` 擇的。

## 屬性 {#section-aace8466566e4cf1a0c5a6c0167245c9}

材料屬性。 如果暈映未定義多個照明映射，則忽略。

## 預設 {#section-c96ecfb232074e80b6a29076f5199403}

`illum=-1`

## 另請參閱 {#section-9132e60381c64aa3a8ed1319690db55e}

[光澤=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
