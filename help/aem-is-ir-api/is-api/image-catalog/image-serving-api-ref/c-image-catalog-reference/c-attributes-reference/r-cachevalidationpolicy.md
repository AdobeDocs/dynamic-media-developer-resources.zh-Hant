---
title: CacheValidationPolicy
description: 伺服器快取驗證原則。 指定伺服器端快取專案驗證的時間。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d54a8ab9-d6b3-4eae-95c6-c4ab6f00ebde
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 3%

---

# CacheValidationPolicy{#cachevalidationpolicy}

伺服器快取驗證原則。 指定伺服器端快取專案驗證的時間。

透過到期日式驗證，會定期檢查來源影像是否已變更。 使用目錄式驗證，只有在`catalog::TimeStamp`值變更後才會檢查來源影像。

使用影像目錄時，建議使用目錄型驗證。 直接參照影像時，不應使用影像目錄，而應使用過期時間型驗證。

## 屬性 {#section-650cbddd81a24c3b8b70479248a45dc9}

列舉。 0代表選取以到期為基礎的驗證，1代表選取以目錄為基礎的快取驗證。

## 預設 {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

如果未定義或空白，則繼承自`default::CacheValidationPolicy`。

## 另請參閱 {#section-a0c922fa519641f2bce05e75e4eb51d0}

[catalog：：TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
