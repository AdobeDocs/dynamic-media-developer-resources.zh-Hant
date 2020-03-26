---
description: 圖層按layer=命令指定的順序組合，其中編號較高的圖層會隱藏編號較低的圖層。
seo-description: 圖層按layer=命令指定的順序組合，其中編號較高的圖層會隱藏編號較低的圖層。
seo-title: 合成畫布
solution: Experience Manager
title: 合成畫布
topic: Scene7 Image Serving - Image Rendering API
uuid: 057b11cb-36f3-40f8-b095-9ad05da858a9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 合成畫布{#the-compositing-canvas}

圖層按layer=命令指定的順序組合，其中編號較高的圖層會隱藏編號較低的圖層。

圖層0是背景圖層，它一律是必要的，並定義了合成影像的大小。 允許對層0使用任何層類型。 必鬚根據內容影像或文字，明確或隱 `size=` 含地定義圖層0的大小。 輸出影像中不包括位於圖層0區域之外的其它圖層的任何區域。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>所有圖層平面化後，複合影像會轉換為最終回應影像，如檢視指令和屬性所 [指定的那樣](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90)。

