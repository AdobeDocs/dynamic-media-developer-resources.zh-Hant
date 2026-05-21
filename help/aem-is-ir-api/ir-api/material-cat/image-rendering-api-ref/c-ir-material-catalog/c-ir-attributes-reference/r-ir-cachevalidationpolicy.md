---
title: CacheValidationPolicy
description: 伺服器快取驗證原則。 指定伺服器端快取專案驗證的時間。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e52577ba-d085-41f5-ad15-48e5a319e344
TQID: 'https://experienceleague.adobe.com/8WipxBM2HngJP5f8LOJmFPA5jZTyJt6Q5P9mZnzDPsY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 114
ht-degree: 2%

---

# CacheValidationPolicy{#cachevalidationpolicy}

伺服器快取驗證原則。 指定伺服器端快取專案驗證的時間。

透過到期日式驗證，會定期檢查原始資料和暈映，以檢視它們是否已變更。 使用目錄式驗證，只有在`catalog::TimeStamp`值變更後才會檢查來源影像。

當同時使用材質和暈映目錄時，建議使用目錄型驗證。 直接透過路徑在影像演算請求中參考暈映時，應使用到期日型驗證。

## 屬性 {#section-46e13cb341eb442c86e0d8292de23ea0}

列舉。 0以選取以到期為基礎的驗證。 1以選取目錄型快取驗證。

## 預設 {#section-e09f3af8b6b3497d963199988dc5345d}

如果未定義或空白，則繼承自`default::CacheValidationPolicy`。

## 另請參閱 {#section-b374e4d908e24af8995b2b376ca1be8b}

[catalog：：TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
