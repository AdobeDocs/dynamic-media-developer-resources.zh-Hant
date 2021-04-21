---
description: Digimarc使用者資訊。 指定Digimarc嵌入的用戶資訊。
solution: Experience Manager
title: DigimarcId
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---


# DigimarcId{#digimarcid}

Digimarc使用者資訊。 指定Digimarc嵌入的用戶資訊。

## 屬性 {#section-1e11a36d9e0b4bf3858c4ab15fe7a272}

5或6個以逗號分隔的整數。 不再使用第三和第四個數字：

`creator-id, creator-pin, durability [ , chroma ]`

`creator-id`和`creator-pin`由Digimarc在購買服務時提供。 未使用的值應留空。

`durability` 指定Digimarc水印嵌入強度。可能為1、2、3或4，其中1表示最弱，4表示最強的耐用性。

將`chroma`設為1，將浮水印編碼為影像的色度資料，或設為0（預設值），將它編碼為明度。 輸出灰階影像時會忽略此設定。

## 預設 {#section-d6ecb6e95a7b4232bd612834ea49e6bc}

如果未定義或為空，則繼承自`default::DigimarcId`。

## 範例 {#section-8469ae1c27b4461da3d53fbabc32d3c5}

指定耐久性設為4的測試Digimarc建立者ID。

`DigimarcId= 404407,32,,,4`

## 另請參閱 {#section-75d4d2afd1df4127b31b1a82f30079d8}

[目錄：:DigimarcInfo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba)
