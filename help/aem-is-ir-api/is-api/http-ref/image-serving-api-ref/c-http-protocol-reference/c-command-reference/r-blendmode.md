---
description: 混合模式. 指定合成圖層時使用的混合類型。 模擬Photoshop市常用的混合模式。 請參閱Photoshop檔案以取得詳細資訊。
solution: Experience Manager
title: blendMode
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 14%

---


# blendMode{#blendmode}

混合模式. 指定合成圖層時使用的混合類型。 模擬Photoshop市常用的混合模式。 請參閱Photoshop檔案以取得詳細資訊。

`blendMode=norm|dissolve|lighten|darken|mult|screen`

## 屬性 {#section-418aad5a417f49929d1953e226e5c8dd}

圖層屬性。 被`layer=0`和`layer=comp`忽略。

## 預設 {#section-69829acc6532448d8612a4a54e86f00e}

`blendMode=norm`

## 範例 {#section-d209dd9c270b469c87558a8910c50b61}

`…&size=200,200&bgColor=191,120,241&…`

`…&layer=1&src=myRootId/myImageId&opac=80&blendMode=dissolve&…`

## 另請參閱 {#section-bc7ccdfcb310441c938c0bde3e00d7b3}

[opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5)
