---
description: 預設重新取樣模式。 指定用於縮放影像資料的預設重採樣和插值屬性。
solution: Experience Manager
title: ResMode
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a604e61e-be38-4819-b5c3-a79843c1678f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 6%

---

# ResMode{#resmode}

預設重新取樣模式。 指定用於縮放影像資料的預設重採樣和插值屬性。

在要求中未指定`resMode=`時使用。

## 屬性 {#section-493f900be522486f97710cebdc4460c2}

列舉。 為`bilin`設為2，為`bicub`設為3，為`sharp2`內插模式設為4（有關詳細資訊，請參閱` [resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)`）。 `sharp` (1)已過時。請改用`sharp2`(4)以獲得最佳結果。

## 預設 {#section-35f980e745fc4d79a2621e8abacc724d}

如果未定義或為空，則從`default::ResMode`繼承。

## 另請參閱 {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
