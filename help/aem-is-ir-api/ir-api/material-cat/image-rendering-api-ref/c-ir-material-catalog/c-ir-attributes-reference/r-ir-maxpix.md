---
description: 回覆影像大小限制。 可傳回給用戶端的回覆影像寬度和高度上限。
seo-description: 回覆影像大小限制。 可傳回給用戶端的回覆影像寬度和高度上限。
seo-title: MaxPix
solution: Experience Manager
title: MaxPix
topic: Scene7 Image Serving - Image Rendering API
uuid: 8fc5e032-cfbb-40b5-9c3a-a2ec1bc4c3e2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 3%

---


# MaxPix{#maxpix}

回覆影像大小限制。 可傳回給用戶端的回覆影像寬度和高度上限。

如果請求會導致寬度和／或高度大於`attribute::MaxSize`的回覆影像，則伺服器會傳回錯誤。

## 屬性 {#section-390c1066b7a748aca3c0b45ad8bdcfb1}

兩個大於0的整數，以逗號分隔。 寬度和高度（以像素為單位）。 也可設定為0,0以允許任何回覆影像大小，且無限制。

## 預設 {#section-45b38dc661854d11b97df5709f4f3434}

繼承自預設值：:MaxPix（如果未定義或為空）。

## 另請參閱 {#section-09cddedde91f43b1ac5828f7e3327c6a}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
