---
description: 回覆影像大小限制。 可返回給客戶端的最大回復影像寬度和高度。
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 0fd990cf-a54f-4574-8328-8988368d5875
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---

# MaxPix{#maxpix}

回覆影像大小限制。 可返回給客戶端的最大回復影像寬度和高度。

如果請求會導致寬度或高度大於`attribute::MaxPix`的回覆影像，則伺服器會傳回錯誤。

## 屬性 {#section-b175425b9e9f48e0b1a71640f6a9e936}

兩個大於0的整數，用逗號分隔。 寬度和高度（像素）。 也可設為`0,0`以允許任何沒有限制的回覆影像大小。

## 預設 {#section-1003537434da432fb2af100ecdbf9d72}

如果未定義或為空，則從`default::MaxPix`繼承。

## 另請參閱 {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
