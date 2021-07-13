---
description: 如果req=img，則複合畫布的大小完全由0層的大小決定。
solution: Experience Manager
title: 複合畫布
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---

# 複合畫布{#the-compositing-canvas}

如果req=img，則複合畫布的大小完全由0層的大小決定。

如果未顯式指定第0層的`size=`，則使用圖層轉換來計算複合畫布的大小（請參見下面）。

如果`req=tmb`，則合成畫布的大小由為層0指定的`size=`決定，或者，如果未指定大小，則合成畫布的大小將設定為視圖直接（請參見下面）。
