---
description: Digimarc使用者資訊。 指定Digimarc嵌入的用戶資訊。
seo-description: Digimarc使用者資訊。 指定Digimarc嵌入的用戶資訊。
seo-title: DigimarcId
solution: Experience Manager
title: DigimarcId
topic: Scene7 Image Serving - Image Rendering API
uuid: 23f1952f-71b7-4b2a-917d-8161ea855ac9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# DigimarcId{#digimarcid}

Digimarc使用者資訊。 指定Digimarc嵌入的用戶資訊。

## 屬性 {#section-1e11a36d9e0b4bf3858c4ab15fe7a272}

5或6個以逗號分隔的整數。 不再使用第三和第四個數字：

`creator-id, creator-pin, durability [ , chroma ]`

購買 `creator-id` 服 `creator-pin` 務時，Digimarc提供此服務。 未使用的值應留空。

`durability` 指定Digimarc水印嵌入強度。 可能為1、2、3或4，其中1表示最弱，4表示最強的耐用性。

設 `chroma` 定為1可將水印編碼為影像的色度資料，或設定為0（預設值）將其編碼為明度。 輸出灰階影像時，會忽略此設定。

## 預設 {#section-d6ecb6e95a7b4232bd612834ea49e6bc}

繼承自 `default::DigimarcId` （如果未定義或為空）。

## 範例 {#section-8469ae1c27b4461da3d53fbabc32d3c5}

指定耐久性設為4的測試Digimarc建立者ID。

`DigimarcId= 404407,32,,,4`

## 另請參閱 {#section-75d4d2afd1df4127b31b1a82f30079d8}

[目錄：:DigimarcInfo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba)
