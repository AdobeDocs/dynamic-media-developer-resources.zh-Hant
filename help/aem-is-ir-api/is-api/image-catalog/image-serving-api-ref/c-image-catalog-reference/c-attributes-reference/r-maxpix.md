---
description: 回覆影像大小限制。 可傳回給用戶端的回覆影像寬度和高度上限。
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 3%

---


# MaxPix{#maxpix}

回覆影像大小限制。 可傳回給用戶端的回覆影像寬度和高度上限。

如果請求會導致寬度或高度大於`attribute::MaxPix`的回覆影像，伺服器會傳回錯誤。

## 屬性 {#section-b175425b9e9f48e0b1a71640f6a9e936}

兩個大於0的整數，以逗號分隔。 寬度和高度（以像素為單位）。 也可設定為`0,0`以允許任何回覆影像大小，且無限制。

## 預設 {#section-1003537434da432fb2af100ecdbf9d72}

如果未定義或為空，則繼承自`default::MaxPix`。

## 另請參閱 {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
