---
description: 混合模式. 指定合成圖層時使用的混合類型。 模擬Photoshop中可用的常用混合模式。 如需詳細資訊，請參閱Photoshop檔案。
solution: Experience Manager
title: blendMode
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 8f0b8b0a-a8ac-4932-986c-5d14d3311f1b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 15%

---

# blendMode{#blendmode}

混合模式. 指定合成圖層時使用的混合類型。 模擬Photoshop中可用的常用混合模式。 如需詳細資訊，請參閱Photoshop檔案。

`blendMode=norm|dissolve|lighten|darken|mult|screen`

## 屬性 {#section-418aad5a417f49929d1953e226e5c8dd}

層屬性。 由`layer=0`和`layer=comp`忽略。

## 預設 {#section-69829acc6532448d8612a4a54e86f00e}

`blendMode=norm`

## 範例 {#section-d209dd9c270b469c87558a8910c50b61}

`…&size=200,200&bgColor=191,120,241&…`

`…&layer=1&src=myRootId/myImageId&opac=80&blendMode=dissolve&…`

## 另請參閱 {#section-bc7ccdfcb310441c938c0bde3e00d7b3}

[opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5)
