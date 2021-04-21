---
description: 預設演算影像大小。 如果請求未使用wid=或hei=明確指定檢視大小，伺服器會限制回覆影像不大於此寬度和高度。
solution: Experience Manager
title: DefaultPix
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 3%

---


# DefaultPix{#defaultpix}

預設演算影像大小。 如果請求未使用wid=或hei=明確指定檢視大小，伺服器會限制回覆影像不大於此寬度和高度。

## 屬性 {#section-9dc5474fc75842308796ab6440b29611}

兩個整數，0或更大，以逗號分隔。 寬度和高度（以像素為單位）。 其中一個或兩個值都可設為0，以保持不受約束。

不適用於巢狀／內嵌請求。

## 預設 {#section-1935781c561e4679aa87a5bcced8df90}

如果未定義或為空，則繼承自`default::DefaultPix`。

## 另請參閱 {#section-d28f18d29ef14692b8706ca08e754f54}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)，屬 [性：:MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)
