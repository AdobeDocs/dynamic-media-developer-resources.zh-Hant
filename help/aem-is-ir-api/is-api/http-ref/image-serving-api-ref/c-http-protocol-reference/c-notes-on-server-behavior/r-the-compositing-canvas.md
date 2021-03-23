---
description: 如果req=img，則複合畫布的大小完全由圖層0的大小決定。
seo-description: 如果req=img，則複合畫布的大小完全由圖層0的大小決定。
seo-title: 合成畫布
solution: Experience Manager
title: 合成畫布
uuid: 7ec2f1b3-61fc-4bfe-96d2-a5946a238e74
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# 合成畫布{#the-compositing-canvas}

如果req=img，則複合畫布的大小完全由圖層0的大小決定。

如果未明確指定圖層0的`size=`，則使用圖層變形來計算構圖畫布的大小（請參閱下面）。

如果`req=tmb`，合成畫布的大小由為圖層0指定的`size=`決定，或者，如果未指定大小，則合成畫布大小會設為檢視方向（請參閱下面）。
