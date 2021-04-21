---
description: 圖層按layer=命令指定的順序組合，其中編號較高的圖層會隱藏編號較低的圖層。
solution: Experience Manager
title: 合成畫布
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# 合成畫布{#the-compositing-canvas}

圖層按layer=命令指定的順序組合，其中編號較高的圖層會隱藏編號較低的圖層。

圖層0是背景圖層，它一律是必要的，並定義了合成影像的大小。 允許對層0使用任何層類型。 必鬚根據內容影像或文字，明確地使用`size=`或隱含地定義圖層0的大小。 輸出影像中不包括位於圖層0區域之外的其它圖層的任何區域。

>[!NOTE]
>
>所有圖層平面化後，複合影像會轉換為最終回應影像，如[檢視命令和屬性](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90)所指定。

