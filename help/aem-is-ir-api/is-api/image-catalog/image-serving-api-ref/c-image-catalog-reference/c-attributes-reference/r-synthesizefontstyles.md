---
description: 啟用合成字型變化。 控制如果要求此種樣式，但在字型圖中找不到，則伺服器應產生錯誤回應或合成粗體、斜體或粗體／斜體字型樣式。
solution: Experience Manager
title: NesighateFontStyles
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---


# NethirateFontStyles{#synthesizefontstyles}

啟用合成字型變化。 控制如果要求此種樣式，但在字型圖中找不到，則伺服器應產生錯誤回應或合成粗體、斜體或粗體／斜體字型樣式。

>[!NOTE]
>
>合成字型樣式通常會產生低品質的轉譯效果，而不是使用實際的字型。

## 屬性 {#section-3205560a74774ebf9c916b07bd15aca6}

標幟. 設為0可停用，設為1可啟用合成字型樣式。

## 預設 {#section-71f94aa65e404d14b441674c040b59e3}

如果未定義或為空，則繼承自`default::SynthesizeFontStyles`。

## 另請參閱 {#section-47a79659cc844272b6d5f36c946e12ac}

[字型圖參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d)
