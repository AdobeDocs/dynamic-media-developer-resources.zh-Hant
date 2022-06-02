---
title: 快取驗證策略
description: 伺服器快取驗證策略。 指定驗證伺服器端快取項的時間。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d54a8ab9-d6b3-4eae-95c6-c4ab6f00ebde
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 4%

---

# 快取驗證策略{#cachevalidationpolicy}

伺服器快取驗證策略。 指定驗證伺服器端快取項的時間。

使用基於過期的驗證，會定期檢查源影像是否已更改。 使用基於目錄的驗證，僅在 `catalog::TimeStamp` 值已更改。

使用映像目錄時，建議使用基於目錄的驗證。 當直接引用影像時，應使用基於過期的驗證，而不使用影像目錄。

## 屬性 {#section-650cbddd81a24c3b8b70479248a45dc9}

枚舉。 0選擇基於過期的驗證，1選擇基於目錄的快取驗證。

## 預設 {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

繼承自 `default::CacheValidationPolicy` 或為空。

## 另請參閱 {#section-a0c922fa519641f2bce05e75e4eb51d0}

[目錄：:TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
