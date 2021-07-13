---
description: 表面粗糙度。 指定材料曲面的相對光澤度。 與「目錄類型」和「目錄光澤」結合使用，以控制3D反射渲染效果。
solution: Experience Manager
title: 粗糙度
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 61d956ec-62dd-4879-877e-2ac422396e2e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 3%

---

# 粗糙度{#roughness}

表面粗糙度。 指定材料曲面的相對光澤度。 與目錄：:Type和目錄：:Gloss一起使用，以控制3D反射渲染效果。

## 屬性 {#section-70c3f2394fd8477ca83a369448907971}

整數。 範圍0...100中的百分比值。 所有材料均可選。 僅用於具有多個反射映射的暈映或具有3D反射功能的暈映。 保留為空或設為–1（如果不已知或不需要）。

## 預設 {#section-c6d5c0613a8745ddbd9f43c8c90b1580}

-1;使用伺服器預設值。

## 另請參閱 {#section-d08b59eb76824226b89c6fdf86bb5ce5}

[rough=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180) ,  [catalog::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb),  [catalog::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
