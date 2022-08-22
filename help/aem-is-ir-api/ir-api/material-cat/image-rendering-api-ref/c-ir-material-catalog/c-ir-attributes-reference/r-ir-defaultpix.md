---
title: 預設影像
description: 預設呈現影像大小。 如果請求未使用wid=或hei=顯式指定視圖大小，則伺服器將回復影像限制為不大於此寬度和高度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d60f2b8c-5213-42ad-8ec9-7e7797d74e09
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 3%

---

# 預設影像{#defaultpix}

預設呈現影像大小。 如果請求未使用wid=或hei=顯式指定視圖大小，則伺服器將回復影像限制為不大於此寬度和高度。

## 屬性 {#section-9dc5474fc75842308796ab6440b29611}

兩個整數，0或更大，用逗號分隔。 寬度和高度（以像素為單位）。 可以將其中一個或兩個值設定為0以保持它們不受約束。

不適用於嵌套/嵌入式請求。

## 預設 {#section-1935781c561e4679aa87a5bcced8df90}

繼承自 `default::DefaultPix` 或為空。

## 另請參閱 {#section-d28f18d29ef14692b8706ca08e754f54}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) 。 [黑=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)。 [屬性：:MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)
