---
description: 預設渲染影像大小。 如果請求未使用wid=或hei=明確指定檢視大小，則伺服器會將回覆影像限制為不大於此寬度和高度。
solution: Experience Manager
title: DefaultPix
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: d60f2b8c-5213-42ad-8ec9-7e7797d74e09
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 3%

---

# DefaultPix{#defaultpix}

預設渲染影像大小。 如果請求未使用wid=或hei=明確指定檢視大小，則伺服器會將回覆影像限制為不大於此寬度和高度。

## 屬性 {#section-9dc5474fc75842308796ab6440b29611}

兩個整數，0或更大，以逗號分隔。 寬度和高度（像素）。 可將任一或兩個值設為0，以保持它們不受約束。

不適用於巢狀/內嵌請求。

## 預設 {#section-1935781c561e4679aa87a5bcced8df90}

如果未定義或為空，則從`default::DefaultPix`繼承。

## 另請參閱 {#section-d28f18d29ef14692b8706ca08e754f54}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ,  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [屬性：:MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)
