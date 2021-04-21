---
description: 預設重新取樣模式。 指定用於縮放影像資料的預設重新採樣和插值屬性。
solution: Experience Manager
title: ResMode
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 5%

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
