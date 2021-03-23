---
description: 伺服器快取驗證原則。 指定何時驗證伺服器端快取條目。
seo-description: 伺服器快取驗證原則。 指定何時驗證伺服器端快取條目。
seo-title: CacheValidationPolicy
solution: Experience Manager
title: CacheValidationPolicy
uuid: 371dadbf-d58e-4214-8050-7e8907b436e3
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---


# CacheValidationPolicy{#cachevalidationpolicy}

伺服器快取驗證原則。 指定何時驗證伺服器端快取條目。

透過基於過期的驗證，系統會定期檢查來源影像是否已變更。 透過型錄式驗證，來源影像只會在`catalog::TimeStamp`值變更後進行檢查。

當使用影像目錄時，建議使用目錄式驗證。 當直接參考影像時，應使用以有效期為基礎的驗證，而不需使用影像目錄。

## 屬性 {#section-650cbddd81a24c3b8b70479248a45dc9}

列舉。 0：選擇基於過期的驗證，1：選擇基於目錄的快取驗證。

## 預設 {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

如果未定義或為空，則繼承自`default::CacheValidationPolicy`。

## 另請參閱 {#section-a0c922fa519641f2bce05e75e4eb51d0}

[目錄：:TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
