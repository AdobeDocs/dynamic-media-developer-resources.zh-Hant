---
description: 影像呈現所使用的記憶體量可能會大不相同，而且取決於實際伺服器負載和使用情況（例如，與許多不同的暈映、暈映的大小和複雜性等）。
solution: Experience Manager
title: 記憶體考量
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 62eaa41c-a61c-4bcd-8dd9-9c3423bf82ef
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# 記憶體考量{#memory-considerations}

影像呈現所使用的記憶體量可能會大不相同，而且取決於實際伺服器負載和使用情況（例如，與許多不同的暈映、暈映的大小和複雜性等）。

為獲得最佳效能，應避免記憶體分頁（交換）。

影像呈現共用影像伺服器的記憶體管理。 使用影像呈現時，應分配額外的記憶體。 30%到50%的物理記憶體可能是合理的。

有關如何更改映像伺服器記憶體分配(ImageServer::PhysicalMemory)的資訊，請參閱映像服務文檔。
