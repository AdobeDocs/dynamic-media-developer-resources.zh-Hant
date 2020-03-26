---
description: 如果req=img，則複合畫布的大小完全由圖層0的大小決定。
seo-description: 如果req=img，則複合畫布的大小完全由圖層0的大小決定。
seo-title: 合成畫布
solution: Experience Manager
title: 合成畫布
topic: Scene7 Image Serving - Image Rendering API
uuid: 7ec2f1b3-61fc-4bfe-96d2-a5946a238e74
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 合成畫布{#the-compositing-canvas}

如果req=img，則複合畫布的大小完全由圖層0的大小決定。

如果未 `size=` 明確指定圖層0，則使用圖層變形來計算構圖畫布的大小（請參閱下面）。

如 `req=tmb`果，合成畫布的大小由為圖層0指定的大小決定，或者，如果未指定 `size=` 大小，則合成畫布的大小會設定為正確的檢視（請參閱下面）。
