---
description: Digimarc使用者資訊。 指定Digimarc內嵌的使用者資訊。
solution: Experience Manager
title: DigimarcId
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac09c8cd-cb68-4b70-b1b4-9d4ca0166c7f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---

# DigimarcId{#digimarcid}

Digimarc使用者資訊。 指定Digimarc內嵌的使用者資訊。

## 屬性 {#section-1e11a36d9e0b4bf3858c4ab15fe7a272}

五或六個逗號分隔的整數。 第三個和第四個數字已不再使用：

`creator-id, creator-pin, durability [ , chroma ]`

購買服務時，Digimarc會提供`creator-id`和`creator-pin`。 未使用的值應留空。

`durability`指定Digimarc浮水印嵌入強度。 可能是1、2、3或4,1表示最弱，4表示最耐用。

設定`chroma`為1可將浮水印編碼至影像的色度資料，或設為0 （預設）可將浮水印編碼至明度。 輸出灰階影像時會忽略此設定。

## 預設 {#section-d6ecb6e95a7b4232bd612834ea49e6bc}

如果未定義或空白，則繼承自`default::DigimarcId`。

## 範例 {#section-8469ae1c27b4461da3d53fbabc32d3c5}

指定耐久性設為4的測試Digimarc建立者ID。

`DigimarcId= 404407,32,,,4`

## 另請參閱 {#section-75d4d2afd1df4127b31b1a82f30079d8}

[catalog：：DigimarcInfo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba)
