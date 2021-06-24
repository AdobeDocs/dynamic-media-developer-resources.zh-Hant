---
description: Digimarc使用者資訊。 指定Digimarc嵌入的用戶資訊。
solution: Experience Manager
title: DigimarcId
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: ac09c8cd-cb68-4b70-b1b4-9d4ca0166c7f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---

# DigimarcId{#digimarcid}

Digimarc使用者資訊。 指定Digimarc嵌入的用戶資訊。

## 屬性 {#section-1e11a36d9e0b4bf3858c4ab15fe7a272}

五或六個以逗號分隔的整數數。 不再使用第三個和第四個數字：

`creator-id, creator-pin, durability [ , chroma ]`

購買服務時，Digimarc會提供`creator-id`和`creator-pin`。 未使用的值應保留空白。

`durability` 指定Digimarc水印嵌入強度。它可以是1、2、3或4，其中1表示最弱和4最強的耐用性。

將`chroma`設定為1可將水印編碼到影像的色度資料中，或將水印編碼到亮度中（預設值）設定為0。 輸出灰度影像時，將忽略此設定。

## 預設 {#section-d6ecb6e95a7b4232bd612834ea49e6bc}

如果未定義或為空，則從`default::DigimarcId`繼承。

## 範例 {#section-8469ae1c27b4461da3d53fbabc32d3c5}

指定耐用性設定為4的測試Digimarc建立器id。

`DigimarcId= 404407,32,,,4`

## 另請參閱 {#section-75d4d2afd1df4127b31b1a82f30079d8}

[目錄：:DigimarcInfo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba)
