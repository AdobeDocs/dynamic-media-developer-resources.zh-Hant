---
description: 表面粗糙度。 指定材料曲面的相對光澤度。 與型錄類型和型錄光澤搭配使用，以控制3D反射演算效果。
solution: Experience Manager
title: 粗糙度
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 3%

---


# 粗糙度{#roughness}

表面粗糙度。 指定材料曲面的相對光澤度。 與型錄：:Type和型錄：:Gloss搭配使用，以控制3D反射演算效果。

## 屬性 {#section-70c3f2394fd8477ca83a369448907971}

整數。 範圍0...100中的百分比值。 所有材料皆可選。 僅用於具有多個反射地圖的暈映或具有3D反射功能的暈映。 保留空白，如果不知道或不需要，則設定為-1。

## 預設 {#section-c6d5c0613a8745ddbd9f43c8c90b1580}

-1;會使用伺服器預設值。

## 另請參閱 {#section-d08b59eb76824226b89c6fdf86bb5ce5}

[rough=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180) , catalog:: [Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), catalog [::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
