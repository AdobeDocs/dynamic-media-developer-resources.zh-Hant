---
description: 如果req=img，則合成畫布的大小完全由層0的大小確定。
solution: Experience Manager
title: 合成畫布
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---

# 合成畫布{#the-compositing-canvas}

如果req=img，則合成畫布的大小完全由層0的大小確定。

如果 `size=` 對於未顯式指定層0，層轉換用於計算合成畫布的大小（請參閱下面）。

如果 `req=tmb`，合成畫布的大小由 `size=` 為層0指定，或者，如果未指定大小，則組合畫布大小將設定為view rect（請參閱下文）。
