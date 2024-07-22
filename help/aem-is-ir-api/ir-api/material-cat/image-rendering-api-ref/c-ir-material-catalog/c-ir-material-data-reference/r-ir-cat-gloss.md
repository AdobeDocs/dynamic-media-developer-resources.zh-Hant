---
description: 曲面光澤度指定材料曲面的相對光澤度。
solution: Experience Manager
title: 光澤
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 72c5d2f9-a7e6-4ad3-aebe-6a1b1fa5453f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 2%

---

# 光澤{#gloss}

曲面光澤度指定材料曲面的相對光澤度。

轉譯器將此值用於下列用途：

* 選取`catalog::Illum`為–1時的照明地圖。
* 控制光澤效果（鏡面反射）與`catalog::Type`一起呈現。
* 控制結合`catalog::Type`和`catalog::Roughness`的3D反射演算效果。

## 屬性 {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

整數。 介於0到100之間的百分比數字。 所有材質均可選用。 僅用於具有多個反射對映的暈映或具有3D反射功能的暈映。 留空或設為–1 （如果不知道或不需要的話）。

## 預設 {#section-2352721073524f1a8d461f64a363aac9}

如果此值設為–1，暈映會提供預設值。

## 另請參閱 {#section-0213bbdb7d6d4974a7c53822957717c1}

[光澤=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) ， [目錄：：Roughtness](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99)， [目錄：：型別](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
