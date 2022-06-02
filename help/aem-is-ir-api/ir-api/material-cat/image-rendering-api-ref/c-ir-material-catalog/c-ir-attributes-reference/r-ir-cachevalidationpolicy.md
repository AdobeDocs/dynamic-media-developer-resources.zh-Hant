---
title: 快取驗證策略
description: 伺服器快取驗證策略。 指定驗證伺服器端快取項的時間。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e52577ba-d085-41f5-ad15-48e5a319e344
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 快取驗證策略{#cachevalidationpolicy}

伺服器快取驗證策略。 指定驗證伺服器端快取項的時間。

使用基於過期的驗證，將定期檢查源材料和小圖，以查看它們是否已更改。 使用基於目錄的驗證，僅在 `catalog::TimeStamp` 值已更改。

當同時使用物料和視頻目錄時，建議使用基於目錄的驗證。 當按路徑直接在影像呈現請求中引用小節時，應使用基於過期的驗證。

## 屬性 {#section-46e13cb341eb442c86e0d8292de23ea0}

枚舉。 0選擇基於過期的驗證。 1選擇基於目錄的快取驗證。

## 預設 {#section-e09f3af8b6b3497d963199988dc5345d}

繼承自 `default::CacheValidationPolicy` 或為空。

## 另請參閱 {#section-b374e4d908e24af8995b2b376ca1be8b}

[目錄：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
