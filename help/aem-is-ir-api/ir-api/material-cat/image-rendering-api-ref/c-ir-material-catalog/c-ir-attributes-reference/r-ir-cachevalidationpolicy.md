---
description: 伺服器快取驗證策略。 指定何時驗證伺服器端快取項目。
solution: Experience Manager
title: CacheValidationPolicy
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e52577ba-d085-41f5-ad15-48e5a319e344
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---

# CacheValidationPolicy{#cachevalidationpolicy}

伺服器快取驗證策略。 指定何時驗證伺服器端快取項目。

透過基於過期的驗證，會定期檢查來源材料和暈映，以查看它們是否已變更。 在基於目錄的驗證中，僅當`catalog::TimeStamp`值更改後才檢查源影像。

同時使用物料和暈映目錄時，建議使用基於目錄的驗證。 當影像轉譯請求中直接依路徑參考暈映時，應使用過期式驗證。

## 屬性 {#section-46e13cb341eb442c86e0d8292de23ea0}

列舉。 0以選取過期驗證。 1選擇基於目錄的快取驗證。

## 預設 {#section-e09f3af8b6b3497d963199988dc5345d}

如果未定義或為空，則從`default::CacheValidationPolicy`繼承。

## 另請參閱 {#section-b374e4d908e24af8995b2b376ca1be8b}

[目錄：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
