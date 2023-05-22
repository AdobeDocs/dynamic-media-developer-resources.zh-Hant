---
description: Digimarc用戶資訊。 指定Digimarc嵌入的用戶資訊。
solution: Experience Manager
title: DigimarcId
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac09c8cd-cb68-4b70-b1b4-9d4ca0166c7f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# DigimarcId{#digimarcid}

Digimarc用戶資訊。 指定Digimarc嵌入的用戶資訊。

## 屬性 {#section-1e11a36d9e0b4bf3858c4ab15fe7a272}

五或六個以逗號分隔的整數。 第三和第四個數字不再使用：

`creator-id, creator-pin, durability [ , chroma ]`

的 `creator-id` 和 `creator-pin` Digimarc在購買服務時提供。 未使用的值應留空。

`durability` 指定Digimarc水印嵌入強度。 它可能為1、2、3或4，其中1表示最弱和4最強耐用。

設定 `chroma` 為1將水印編碼到影像的色度資料中，為0（預設）將水印編碼到亮度中。 輸出灰度影像時將忽略此設定。

## 預設 {#section-d6ecb6e95a7b4232bd612834ea49e6bc}

繼承自 `default::DigimarcId` 或為空。

## 範例 {#section-8469ae1c27b4461da3d53fbabc32d3c5}

指定耐久性設定為4的testDigimarc建立器ID。

`DigimarcId= 404407,32,,,4`

## 另請參閱 {#section-75d4d2afd1df4127b31b1a82f30079d8}

[目錄：:DigimarcInfo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba)
