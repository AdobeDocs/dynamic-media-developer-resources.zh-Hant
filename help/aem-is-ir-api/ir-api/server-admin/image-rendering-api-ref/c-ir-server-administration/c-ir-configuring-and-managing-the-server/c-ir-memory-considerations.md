---
description: 影像呈現使用的記憶體量可能差異很大，並且高度取決於實際伺服器負載和使用情況（例如，與許多不同的小格、小格的大小和複雜性等）。
solution: Experience Manager
title: 記憶體注意事項
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 62eaa41c-a61c-4bcd-8dd9-9c3423bf82ef
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---

# 記憶體注意事項{#memory-considerations}

影像呈現使用的記憶體量可能差異很大，並且高度取決於實際伺服器負載和使用情況（例如，與許多不同的小格、小格的大小和複雜性等）。

為獲得最佳效能，應避免記憶體分頁（交換）。

影像呈現共用影像伺服器的記憶體管理。 使用「影像渲染」時，應分配額外的記憶體。 30%到50%的物理記憶體可能是合理的。

有關如何更改映像伺服器記憶體分配(ImageServer::PhysicalMemory)的資訊，請參閱映像服務文檔。
