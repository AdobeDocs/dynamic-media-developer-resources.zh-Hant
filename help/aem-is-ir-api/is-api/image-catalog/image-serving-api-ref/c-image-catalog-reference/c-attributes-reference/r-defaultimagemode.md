---
description: 預設影像模式。 選擇在找不到請求中指定的影像時應用預設影像的方式。
solution: Experience Manager
title: 預設影像模式
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b30ce72f-7c74-407c-bd4a-042b84c469e9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 2%

---

# 預設影像模式{#defaultimagemode}

預設影像模式。 選擇在找不到請求中指定的影像時應用預設影像的方式。

## 屬性 {#section-7fa8acb63540490d9f5186231b5e77c3}

枚舉。 「0」替換整個複合影像，即使缺失的影像只是幾層中的一層；「1」，用預設影像替換每個丟失的圖層源影像，並像往常一樣返回複合影像。

## 限制 {#section-04cb0d50e8914564a8d226d0d4663c8b}

影像服務恢復為 `DefaultImageMode=0` 嵌套影像呈現、FXG或 `req=set` 請求失敗。

## 預設 {#section-9e318524a2a5496386901286748c7ee7}

繼承自 `default::DefaultImage` 或為空。

## 另請參閱 {#section-fddce1d27a0c43fb8b4d891f76ac5a52}

[defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433) 。 [屬性：:DefaultImage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
