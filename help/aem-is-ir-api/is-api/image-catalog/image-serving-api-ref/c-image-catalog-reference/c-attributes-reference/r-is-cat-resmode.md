---
description: 預設重新取樣模式。 指定用於縮放影像資料的預設重新採樣和插值屬性。
seo-description: 預設重新取樣模式。 指定用於縮放影像資料的預設重新採樣和插值屬性。
seo-title: ResMode
solution: Experience Manager
title: ResMode
topic: Scene7 Image Serving - Image Rendering API
uuid: 14d184bd-6664-4f8f-b551-a92cb92a0d84
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ResMode{#resmode}

預設重新取樣模式。 指定用於縮放影像資料的預設重新採樣和插值屬性。

在請求 `resMode=` 中未指定時使用。

## 屬性 {#section-493f900be522486f97710cebdc4460c2}

列舉。 若為插值模 `bilin`式，請設 `bicub`定為2、3或4 `sharp2` (如需詳細資訊， ` [resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)` 請參閱)。 `sharp` (1)已過時。 請改 `sharp2` 用(4)以取得最佳結果。

## 預設 {#section-35f980e745fc4d79a2621e8abacc724d}

繼承自 `default::ResMode` （如果未定義或為空）。

## 另請參閱 {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
