---
title: 合成字型樣式
description: 啟用合成字型變體。 控制伺服器是否應該產生錯誤回應，或合成粗體、斜體或粗體/斜體字型樣式（如果要求這種樣式，但在字型地圖中找不到）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08f20748-71c7-4b9f-9b45-70352f9abf35
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 2%

---

# 合成字型樣式{#synthesizefontstyles}

啟用合成字型變體。 控制伺服器是否應該產生錯誤回應，或合成粗體、斜體或粗體/斜體字型樣式（如果要求這種樣式，但在字型地圖中找不到）。

>[!NOTE]
>
>合成字型樣式通常會產生比使用實際字型來呈現這類樣式低品質的呈現。

## 屬性 {#section-3205560a74774ebf9c916b07bd15aca6}

標幟。 設為0會停用並設為1會啟用合成字型樣式。

## 預設 {#section-71f94aa65e404d14b441674c040b59e3}

如果未定義或空白，則繼承自`default::SynthesizeFontStyles`。

## 另請參閱 {#section-47a79659cc844272b6d5f36c946e12ac}

[字型地圖參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d)
