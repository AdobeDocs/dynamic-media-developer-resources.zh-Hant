---
description: 答復影像大小限制。 可返回給客戶端的最大回復影像寬度和高度。
solution: Experience Manager
title: 最大圖
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0fd990cf-a54f-4574-8328-8988368d5875
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 3%

---

# 最大圖{#maxpix}

答復影像大小限制。 可返回給客戶端的最大回復影像寬度和高度。

如果請求會導致寬度或高度大於的應答影像，則伺服器返回錯誤 `attribute::MaxPix`。

## 屬性 {#section-b175425b9e9f48e0b1a71640f6a9e936}

兩個大於0的整數，用逗號分隔。 寬度和高度（以像素為單位）。 也可設定為 `0,0` 允許任何無限制的回復影像大小。

## 預設 {#section-1003537434da432fb2af100ecdbf9d72}

繼承自 `default::MaxPix` 或為空。

## 另請參閱 {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) 。 [黑=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
