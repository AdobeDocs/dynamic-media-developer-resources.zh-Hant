---
description: 內嵌色彩描述檔。 指定是否應將工作中的ICC色彩描述檔或以icc=指定的描述檔內嵌在回覆影像中。
seo-description: 內嵌色彩描述檔。 指定是否應將工作中的ICC色彩描述檔或以icc=指定的描述檔內嵌在回覆影像中。
seo-title: iccEmbed
solution: Experience Manager
title: iccEmbed
topic: Scene7 Image Serving - Image Rendering API
uuid: ccd3fd2f-6f73-4725-a51a-9daf643d71af
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 3%

---


# iccEmbed{#iccembed}

內嵌色彩描述檔。 指定是否應將工作中的ICC色彩描述檔或以icc=指定的描述檔內嵌在回覆影像中。

`iccEmbed=0|1`

## 屬性 {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

請求屬性。 如果沒有可用於嵌入的配置檔案，則忽略。

## 預設 {#section-01948f6cd7a2415091004cd7526436c7}

`iccEmbed=0`，因為輸出影像中沒有內嵌ICC描述檔。如果輸出影像格式不支援嵌入ICC配置檔案，則忽略。

有關詳細資訊，請參見[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)。

## 另請參閱 {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[attribute::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) , [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
