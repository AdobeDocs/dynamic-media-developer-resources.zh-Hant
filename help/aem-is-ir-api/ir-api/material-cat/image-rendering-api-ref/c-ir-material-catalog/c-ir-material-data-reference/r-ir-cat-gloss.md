---
description: 曲面光澤度指定材料曲面的相對光澤度。
solution: Experience Manager
title: 光澤
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 72c5d2f9-a7e6-4ad3-aebe-6a1b1fa5453f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 2%

---

# 光澤{#gloss}

曲面光澤度指定材料曲面的相對光澤度。

該值由呈現器用於以下目的：

* 選擇光照映射 `catalog::Illum` 是–1。
* 控制光澤效果（鏡面反射）與結合的渲染 `catalog::Type`。
* 控制3D反射渲染效果與 `catalog::Type` 和 `catalog::Roughness`。

## 屬性 {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

整數。 0..100範圍內的百分比數字。 可選，適用於所有材料。 僅用於具有多個反射映射的小角或具有3D反射功能的小角。 保留為空，如果未知或不需要，則將其設定為–1。

## 預設 {#section-2352721073524f1a8d461f64a363aac9}

如果此值設定為–1，則視圖提供預設值。

## 另請參閱 {#section-0213bbdb7d6d4974a7c53822957717c1}

[光澤=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) 。 [目錄：：粗糙度](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99)。 [目錄：：類型](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
