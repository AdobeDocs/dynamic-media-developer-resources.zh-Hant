---
description: 影像演算所使用的記憶體數量可能大相逕庭，且很大程度上取決於伺服器實際負載和使用狀況（例如，很少與許多不同暈映、暈映的大小和複雜度等等）。
solution: Experience Manager
title: 記憶體考量事項
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 62eaa41c-a61c-4bcd-8dd9-9c3423bf82ef
TQID: 'https://experienceleague.adobe.com/l41dx4mMn82TvImVVCJJKgJZbP-mWT5KbnzfZ5xFJqg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 129
ht-degree: 0%

---

# 記憶體考量事項{#memory-considerations}

影像演算所使用的記憶體數量可能大相逕庭，且很大程度上取決於伺服器實際負載和使用狀況（例如，很少與許多不同暈映、暈映的大小和複雜度等等）。

為獲得最佳效能，應避免記憶體分頁（交換）。

影像演算共用影像伺服器的記憶體管理。 使用影像演算時，應配置額外的記憶體。 30%至50%的實體記憶體可能是合理的。

如需有關如何變更影像伺服器記憶體配置(ImageServer：：PhysicalMemory)的資訊，請參閱「影像伺服」檔案。
