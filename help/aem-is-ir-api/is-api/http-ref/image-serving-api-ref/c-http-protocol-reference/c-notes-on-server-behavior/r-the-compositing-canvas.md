---
description: 如果req=img，合成畫布的大小完全由圖層0的大小決定。
solution: Experience Manager
title: 合成畫布
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# 合成畫布{#the-compositing-canvas}

如果req=img，合成畫布的大小完全由圖層0的大小決定。

如果未明確指定圖層0的`size=`，則會使用圖層轉換來計算合成畫布的大小（請參閱下文）。

如果是`req=tmb`，則合成畫布的大小是由為圖層0指定的`size=`決定，如果未指定大小，則合成畫布大小會設定為檢視矩形（請參閱下文）。
