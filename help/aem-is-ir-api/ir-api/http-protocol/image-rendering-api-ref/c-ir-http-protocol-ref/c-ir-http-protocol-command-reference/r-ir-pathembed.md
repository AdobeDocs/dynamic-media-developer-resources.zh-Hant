---
description: 內嵌路徑資料。 指定是否應將內嵌於暈映中的Photoshop路徑納入回應影像中。
solution: Experience Manager
title: pathEmbed
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 66cc57ef-964e-4062-bb66-efeda15be744
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 3%

---

# pathEmbed{#pathembed}

內嵌路徑資料。 指定是否應將內嵌於暈映中的Photoshop路徑納入回應影像中。

`pathEmbed=0|1`

## 屬性 {#section-be50b6d1ebd14a9c93f80ac338b44bfc}

要求屬性。 如果暈映不包含路徑資料，則會忽略。 如有必要，路徑資料會縮放至`wid=`及/或`hei=`。

如果輸出影像格式不支援路徑嵌入，則忽略。 有關支援路徑嵌入的輸出影像格式的清單，請參閱`fmt=`的說明。

## 預設 {#section-3be88ed9053b48919ff33af9418078cc}

`pathEmbed=0`，不會將路徑嵌入輸出影像中。

## 另請參閱 {#section-4e6151658c384b6f9d0446f55dde7b7f}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c),  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
