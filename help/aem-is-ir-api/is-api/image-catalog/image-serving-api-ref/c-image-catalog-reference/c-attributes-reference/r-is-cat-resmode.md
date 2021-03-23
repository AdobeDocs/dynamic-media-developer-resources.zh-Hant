---
description: 預設重新取樣模式。 指定用於縮放影像資料的預設重新採樣和插值屬性。
seo-description: 預設重新取樣模式。 指定用於縮放影像資料的預設重新採樣和插值屬性。
seo-title: ResMode
solution: Experience Manager
title: ResMode
uuid: 14d184bd-6664-4f8f-b551-a92cb92a0d84
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 4%

---


# ResMode{#resmode}

預設重新取樣模式。 指定用於縮放影像資料的預設重新採樣和插值屬性。

在請求中未指定`resMode=`時使用。

## 屬性 {#section-493f900be522486f97710cebdc4460c2}

列舉。 設為2表示`bilin`,3表示`bicub`,4表示`sharp2`內插模式（如需詳細資訊，請參閱` [resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)`）。 `sharp` (1)已過時。請改用`sharp2`(4)以取得最佳結果。

## 預設 {#section-35f980e745fc4d79a2621e8abacc724d}

如果未定義或為空，則繼承自`default::ResMode`。

## 另請參閱 {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
