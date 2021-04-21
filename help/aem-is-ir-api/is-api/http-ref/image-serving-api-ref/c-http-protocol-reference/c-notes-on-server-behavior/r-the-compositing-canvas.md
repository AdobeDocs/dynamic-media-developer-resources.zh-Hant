---
description: 如果req=img，則複合畫布的大小完全由圖層0的大小決定。
solution: Experience Manager
title: 合成畫布
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---


# 合成畫布{#the-compositing-canvas}

如果req=img，則複合畫布的大小完全由圖層0的大小決定。

如果未明確指定圖層0的`size=`，則使用圖層變形來計算構圖畫布的大小（請參閱下面）。

如果`req=tmb`，合成畫布的大小由為圖層0指定的`size=`決定，或者，如果未指定大小，則合成畫布大小會設為檢視方向（請參閱下面）。
