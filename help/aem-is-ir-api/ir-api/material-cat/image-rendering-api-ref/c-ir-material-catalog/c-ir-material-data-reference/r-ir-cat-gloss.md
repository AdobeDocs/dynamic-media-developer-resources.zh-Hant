---
description: 曲面光澤度指定材料曲面的相對光澤度。
solution: Experience Manager
title: 光澤
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---


# Gloss{#gloss}

曲面光澤度指定材料曲面的相對光澤度。

此值由渲染器用於以下用途：

* 當`catalog::Illum`為-1時，選擇照明映射。
* 控制光澤效果（鏡面反射）演算與`catalog::Type`結合。
* 控制3D反射演算效果，並搭配`catalog::Type`和`catalog::Roughness`。

## 屬性 {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

整數。 0...100範圍內的百分比數字。 所有材料皆可選。 僅用於具有多個反射地圖的暈映或具有3D反射功能的暈映。 保留空白，如果不知道或不需要，則設定為-1。

## 預設 {#section-2352721073524f1a8d461f64a363aac9}

如果此值設為-1，則暈映會提供預設值。

## 另請參閱 {#section-0213bbdb7d6d4974a7c53822957717c1}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) , catalog:: [Ruance](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99), catalog:: [Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
