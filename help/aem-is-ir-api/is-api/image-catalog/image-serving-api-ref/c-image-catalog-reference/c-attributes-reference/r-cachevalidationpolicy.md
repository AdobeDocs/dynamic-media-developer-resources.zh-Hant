---
description: 伺服器快取驗證策略。 指定何時驗證伺服器端快取項目。
solution: Experience Manager
title: CacheValidationPolicy
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: d54a8ab9-d6b3-4eae-95c6-c4ab6f00ebde
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---

# CacheValidationPolicy{#cachevalidationpolicy}

伺服器快取驗證策略。 指定何時驗證伺服器端快取項目。

使用基於過期的驗證，會定期檢查源映像是否已更改。 在基於目錄的驗證中，僅當`catalog::TimeStamp`值更改後才檢查源影像。

使用影像目錄時，建議使用目錄式驗證。 直接參考影像時，應使用過期式驗證，而不使用影像目錄。

## 屬性 {#section-650cbddd81a24c3b8b70479248a45dc9}

列舉。 0選擇基於過期的驗證，1選擇基於目錄的快取驗證。

## 預設 {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

如果未定義或為空，則從`default::CacheValidationPolicy`繼承。

## 另請參閱 {#section-a0c922fa519641f2bce05e75e4eb51d0}

[目錄：:TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
