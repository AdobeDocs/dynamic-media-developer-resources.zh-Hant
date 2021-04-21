---
description: 「影像演算」使用的記憶體量可能會大不相同，而且會高度依實際伺服器負載和使用量而異（例如，與許多不同的暈映、暈映的大小和複雜度等）。
solution: Experience Manager
title: 記憶體注意事項
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---


# 記憶體注意事項{#memory-considerations}

「影像演算」使用的記憶體量可能會大不相同，而且會高度依實際伺服器負載和使用量而異（例如，與許多不同的暈映、暈映的大小和複雜度等）。

為獲得最佳效能，應避免記憶體分頁（調換）。

「影像演算」可共用影像伺服器的記憶體管理。 使用「影像演算」時，應分配額外的記憶體。 30%到50%的物理記憶體是合理的。

有關如何更改映像伺服器記憶體分配(ImageServer::PhysicalMemory)的資訊，請參閱映像服務文檔。
