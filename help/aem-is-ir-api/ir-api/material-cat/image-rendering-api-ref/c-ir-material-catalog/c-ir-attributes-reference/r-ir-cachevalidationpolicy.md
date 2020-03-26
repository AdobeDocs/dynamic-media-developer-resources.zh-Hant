---
description: 伺服器快取驗證原則。 指定何時驗證伺服器端快取條目。
seo-description: 伺服器快取驗證原則。 指定何時驗證伺服器端快取條目。
seo-title: CacheValidationPolicy
solution: Experience Manager
title: CacheValidationPolicy
topic: Scene7 Image Serving - Image Rendering API
uuid: 299dd5fe-9a0c-43df-a4c8-6b9e9c24003b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CacheValidationPolicy{#cachevalidationpolicy}

伺服器快取驗證原則。 指定何時驗證伺服器端快取條目。

透過基於有效期的驗證，會定期檢查來源資料和暈映，以查看它們是否已變更。 透過型錄驗證，只有在值變更後，才會檢查來 `catalog::TimeStamp` 源影像。

同時使用材質和暈映型錄時，建議使用型錄式驗證。 當透過路徑直接參照影像演算請求中的暈映時，應使用期限型驗證。

## 屬性 {#section-46e13cb341eb442c86e0d8292de23ea0}

列舉。 0，以選取過期驗證。 1：選擇基於目錄的快取驗證。

## 預設 {#section-e09f3af8b6b3497d963199988dc5345d}

繼承自 `default::CacheValidationPolicy` （如果未定義或為空）。

## 另請參閱 {#section-b374e4d908e24af8995b2b376ca1be8b}

[目錄：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
