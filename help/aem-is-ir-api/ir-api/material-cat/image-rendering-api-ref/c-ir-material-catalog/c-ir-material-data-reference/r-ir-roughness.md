---
description: 表面粗糙度。 指定材料曲面的相對光澤度。 與目錄「型別」和目錄「光澤」搭配使用以控制3D反射彩現效果。
solution: Experience Manager
title: 粗糙度
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 61d956ec-62dd-4879-877e-2ac422396e2e
TQID: 'https://experienceleague.adobe.com/YvUmUkOLzzbM7Zs-7T35rwYRNrUeh6-QXW339AA3R8Q'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 106
ht-degree: 2%

---

# 粗糙度{#roughness}

表面粗糙度。 指定材料曲面的相對光澤度。 與catalog：：Type和catalog：：Gloss搭配使用可控制3D反射彩現效果。

## 屬性 {#section-70c3f2394fd8477ca83a369448907971}

整數。 介於0到100之間的百分比值。 所有材質均可選用。 僅用於具有多個反射對映的暈映或具有3D反射功能的暈映。 留空或設為–1 （如果不知道或不需要的話）。

## 預設 {#section-c6d5c0613a8745ddbd9f43c8c90b1580}

-1；使用伺服器預設值。

## 另請參閱 {#section-d08b59eb76824226b89c6fdf86bb5ce5}

[rough=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180) ， [目錄：：Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb)， [目錄：：型別](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
