---
description: 混合模式. 指定合成圖層時使用的混合類型。 模擬Photoshop中常用的混合模式。 如需詳細資訊，請參閱Photoshop檔案。
seo-description: 混合模式. 指定合成圖層時使用的混合類型。 模擬Photoshop中常用的混合模式。 如需詳細資訊，請參閱Photoshop檔案。
seo-title: blendMode
solution: Experience Manager
title: blendMode
topic: Scene7 Image Serving - Image Rendering API
uuid: 9ae30495-c10b-4c55-968e-effb602a0857
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# blendMode{#blendmode}

混合模式. 指定合成圖層時使用的混合類型。 模擬Photoshop中常用的混合模式。 如需詳細資訊，請參閱Photoshop檔案。

`blendMode=norm|dissolve|lighten|darken|mult|screen`

## 屬性 {#section-418aad5a417f49929d1953e226e5c8dd}

圖層屬性。 被和忽 `layer=0` 略 `layer=comp`。

## 預設 {#section-69829acc6532448d8612a4a54e86f00e}

`blendMode=norm`

## 範例 {#section-d209dd9c270b469c87558a8910c50b61}

`…&size=200,200&bgColor=191,120,241&…`

`…&layer=1&src=myRootId/myImageId&opac=80&blendMode=dissolve&…`

## 另請參閱 {#section-bc7ccdfcb310441c938c0bde3e00d7b3}

[opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5)
