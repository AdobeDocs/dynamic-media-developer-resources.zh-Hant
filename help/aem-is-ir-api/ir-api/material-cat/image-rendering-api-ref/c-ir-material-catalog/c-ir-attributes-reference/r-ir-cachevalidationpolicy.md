---
description: 伺服器快取驗證原則。 指定何時驗證伺服器端快取條目。
solution: Experience Manager
title: CacheValidationPolicy
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

---


# CacheValidationPolicy{#cachevalidationpolicy}

伺服器快取驗證原則。 指定何時驗證伺服器端快取條目。

透過基於有效期的驗證，會定期檢查來源資料和暈映，以查看它們是否已變更。 透過型錄式驗證，來源影像只會在`catalog::TimeStamp`值變更後進行檢查。

同時使用材質和暈映型錄時，建議使用型錄式驗證。 當透過路徑直接參照影像演算請求中的暈映時，應使用期限型驗證。

## 屬性 {#section-46e13cb341eb442c86e0d8292de23ea0}

列舉。 0，以選取過期驗證。 1：選擇基於目錄的快取驗證。

## 預設 {#section-e09f3af8b6b3497d963199988dc5345d}

如果未定義或為空，則繼承自`default::CacheValidationPolicy`。

## 另請參閱 {#section-b374e4d908e24af8995b2b376ca1be8b}

[目錄：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
