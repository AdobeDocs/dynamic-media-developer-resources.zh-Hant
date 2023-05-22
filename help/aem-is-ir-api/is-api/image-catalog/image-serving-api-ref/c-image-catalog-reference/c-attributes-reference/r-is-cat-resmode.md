---
title: Res模式
description: 預設重採樣模式。 指定用於縮放影像資料的預設重採樣和插值屬性。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a604e61e-be38-4819-b5c3-a79843c1678f
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 5%

---

# Res模式{#resmode}

預設重採樣模式。 指定用於縮放影像資料的預設重採樣和插值屬性。

使用時間 `resMode=` 未在請求中指定。

## 屬性 {#section-493f900be522486f97710cebdc4460c2}

枚舉。 設定為2 `bilin`, 3 `bicub`，或4 `sharp2` 插值模式 [resMode=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-resmode.md) )。 `sharp` (1)不建議使用。 使用 `sharp2` （四）取得最佳效果。

## 預設 {#section-35f980e745fc4d79a2621e8abacc724d}

繼承自 `default::ResMode` 或為空。

## 另請參閱 {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
