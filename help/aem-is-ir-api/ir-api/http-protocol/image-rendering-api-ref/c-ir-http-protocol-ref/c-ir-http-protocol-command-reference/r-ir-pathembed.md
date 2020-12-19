---
description: 內嵌路徑資料。 指定是否應將內嵌在暈映中的Photoshop路徑包含在回應影像中。
seo-description: 內嵌路徑資料。 指定是否應將內嵌在暈映中的Photoshop路徑包含在回應影像中。
seo-title: pathEmbed
solution: Experience Manager
title: pathEmbed
topic: Scene7 Image Serving - Image Rendering API
uuid: d40ea1b5-f2d3-4f81-b96f-abb4eb7eb2b3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 3%

---


# pathEmbed{#pathembed}

內嵌路徑資料。 指定是否應將內嵌在暈映中的Photoshop路徑包含在回應影像中。

`pathEmbed=0|1`

## 屬性 {#section-be50b6d1ebd14a9c93f80ac338b44bfc}

請求屬性。 如果暈映不包含路徑資料，則忽略。 如果需要，路徑資料將縮放為`wid=`和／或`hei=`。

如果輸出影像格式不支援路徑內嵌，則會忽略。 有關支援路徑嵌入的輸出影像格式的清單，請參閱`fmt=`的說明。

## 預設 {#section-3be88ed9053b48919ff33af9418078cc}

`pathEmbed=0`，因為輸出影像中沒有內嵌路徑。

## 另請參閱 {#section-4e6151658c384b6f9d0446f55dde7b7f}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c),  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
