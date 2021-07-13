---
description: 啟用合成的字型變化。 控制如果請求了粗體、斜體或粗體/斜體字型樣式但在字型映射中找不到時，伺服器應生成錯誤響應還是合成粗體、斜體或粗體/斜體字型樣式。
solution: Experience Manager
title: SynethrotingFontStyles
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08f20748-71c7-4b9f-9b45-70352f9abf35
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---

# SynethrotingFontStyles{#synthesizefontstyles}

啟用合成的字型變化。 控制如果請求了粗體、斜體或粗體/斜體字型樣式但在字型映射中找不到時，伺服器應生成錯誤響應還是合成粗體、斜體或粗體/斜體字型樣式。

>[!NOTE]
>
>合成字型樣式通常會導致畫質較低，而不是使用實際字型來呈現這些樣式。

## 屬性 {#section-3205560a74774ebf9c916b07bd15aca6}

標幟. 設為0可停用，設為1可啟用合成字型樣式。

## 預設 {#section-71f94aa65e404d14b441674c040b59e3}

如果未定義或為空，則從`default::SynthesizeFontStyles`繼承。

## 另請參閱 {#section-47a79659cc844272b6d5f36c946e12ac}

[字型圖參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d)
