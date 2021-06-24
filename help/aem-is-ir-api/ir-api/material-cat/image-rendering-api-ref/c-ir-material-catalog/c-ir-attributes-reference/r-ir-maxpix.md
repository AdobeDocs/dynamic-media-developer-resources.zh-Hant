---
description: 回覆影像大小限制。 可返回給客戶端的最大回復影像寬度和高度。
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 48239519-7935-45e4-ae36-5e687a356cc1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 3%

---

# MaxPix{#maxpix}

回覆影像大小限制。 可返回給客戶端的最大回復影像寬度和高度。

如果請求會導致寬度和/或高度大於`attribute::MaxSize`的回覆影像，則伺服器會傳回錯誤。

## 屬性 {#section-390c1066b7a748aca3c0b45ad8bdcfb1}

兩個大於0的整數，用逗號分隔。 寬度和高度（像素）。 也可設為0,0以允許任何回覆影像大小而不受限制。

## 預設 {#section-45b38dc661854d11b97df5709f4f3434}

繼承自預設值：:MaxPix（如果未定義）或為空。

## 另請參閱 {#section-09cddedde91f43b1ac5828f7e3327c6a}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ,  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
