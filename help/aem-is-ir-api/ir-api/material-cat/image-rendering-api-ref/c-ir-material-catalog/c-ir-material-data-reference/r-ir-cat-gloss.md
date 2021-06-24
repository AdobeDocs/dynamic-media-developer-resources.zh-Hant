---
description: 曲面光澤度指定材料曲面的相對光澤度。
solution: Experience Manager
title: 光澤
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 72c5d2f9-a7e6-4ad3-aebe-6a1b1fa5453f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---

# 光澤{#gloss}

曲面光澤度指定材料曲面的相對光澤度。

此值供轉譯器用於下列用途：

* 當`catalog::Illum`為–1時，選擇照明映射。
* 控制光澤效果（鏡面反射）與`catalog::Type`一起呈現。
* 控制與`catalog::Type`和`catalog::Roughness`結合的3D反射渲染效果。

## 屬性 {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

整數。 範圍0...100中的百分比數。 所有材料均可選。 僅用於具有多個反射映射的暈映或具有3D反射功能的暈映。 保留為空或設為–1（如果不已知或不需要）。

## 預設 {#section-2352721073524f1a8d461f64a363aac9}

如果此值設定為–1，則暈映器會提供預設值。

## 另請參閱 {#section-0213bbdb7d6d4974a7c53822957717c1}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) ，目 [錄：：粗糙度](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99), [目錄：:Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
