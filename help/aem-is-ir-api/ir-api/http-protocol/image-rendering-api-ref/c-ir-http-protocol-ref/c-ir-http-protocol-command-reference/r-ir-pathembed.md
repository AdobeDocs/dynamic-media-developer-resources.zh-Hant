---
title: 路徑嵌入
description: 嵌入路徑資料。 指定是否應將嵌入在視頻中的Photoshop路徑包含在響應影像中。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 66cc57ef-964e-4062-bb66-efeda15be744
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---

# 路徑嵌入{#pathembed}

嵌入路徑資料。 指定是否應將嵌入在視頻中的Photoshop路徑包含在響應影像中。

`pathEmbed=0|1`

## 屬性 {#section-be50b6d1ebd14a9c93f80ac338b44bfc}

請求屬性。 如果視圖不包含路徑資料，則忽略。 路徑資料將縮放到 `wid=` 和/或 `hei=` 必要時。

如果輸出影像格式不支援路徑嵌入，則忽略。 請參閱 `fmt=` 的子菜單。

## 預設 {#section-3be88ed9053b48919ff33af9418078cc}

`pathEmbed=0`，以在輸出影像中不嵌入路徑。

## 另請參閱 {#section-4e6151658c384b6f9d0446f55dde7b7f}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)。 [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)。 [黑=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
