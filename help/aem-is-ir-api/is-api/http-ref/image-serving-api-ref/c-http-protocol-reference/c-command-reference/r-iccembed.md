---
title: iccEmbed
description: 內嵌色彩設定檔。 指定回覆影像中應該嵌入正在運作的ICC色彩設定檔，或是以icc=指定的設定檔。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bc5637f6-5452-4bfb-bf30-def6f153f4ad
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# iccEmbed{#iccembed}

內嵌色彩設定檔。 指定回覆影像中應該嵌入正在運作的ICC色彩設定檔，或是以icc=指定的設定檔。

`iccEmbed=0|1`

## 屬性 {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

要求屬性。 如果沒有可供嵌入的設定檔，則會忽略。

## 預設 {#section-01948f6cd7a2415091004cd7526436c7}

`iccEmbed=0`，輸出影像中不內嵌ICC設定檔。 如果輸出影像格式不支援內嵌ICC設定檔，則忽略。

另請參閱 [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) 以取得詳細資訊。

## 另請參閱 {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[attribute：：IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) ， [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)， [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
