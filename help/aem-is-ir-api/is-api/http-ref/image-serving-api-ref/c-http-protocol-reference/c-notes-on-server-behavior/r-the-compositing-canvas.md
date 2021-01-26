---
description: 如果req=img，則複合畫布的大小完全由圖層0的大小決定。
seo-description: 如果req=img，則複合畫布的大小完全由圖層0的大小決定。
seo-title: 合成畫布
solution: Experience Manager
title: 合成畫布
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 7ec2f1b3-61fc-4bfe-96d2-a5946a238e74
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---


# 合成畫布{#the-compositing-canvas}

如果req=img，則複合畫布的大小完全由圖層0的大小決定。

如果未明確指定圖層0的`size=`，則使用圖層變形來計算構圖畫布的大小（請參閱下面）。

如果`req=tmb`，合成畫布的大小由為圖層0指定的`size=`決定，或者，如果未指定大小，則合成畫布大小會設為檢視方向（請參閱下面）。
