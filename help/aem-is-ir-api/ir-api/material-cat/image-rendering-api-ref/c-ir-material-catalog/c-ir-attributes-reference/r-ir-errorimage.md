---
description: 錯誤響應影像。 影像呈現通常會在發生錯誤時傳回帶有文字訊息的錯誤狀態。 屬性ErrorImage允許配置要在發生錯誤時返回的影像。
solution: Experience Manager
title: ErrorImage *
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: ed48482f-79b0-4c81-b5cd-cf997f27d3ab
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 1%

---

# ErrorImage *{#errorimage}

錯誤響應影像。 影像呈現通常會在發生錯誤時傳回帶有文字訊息的錯誤狀態。 屬性：:ErrorImage允許配置要在發生錯誤時返回的影像。

發生錯誤時，伺服器會先嘗試將`ImageRendering::attribute::ErrorImage`的值解譯為簡單的影像檔案路徑。 如果無法開啟檔案，則會將屬性值和錯誤詳細資訊發送到影像伺服器，該伺服器將按照`ImageServing::attribute::ErrorImage`中所述進行處理。 如果「影像伺服器」未傳回有效的回應影像，則會將標準HTTP錯誤狀態和文字訊息傳送至用戶端。

傳回的錯誤影像為HTTP狀態200。

## 屬性 {#section-4a4a7e37ed11483db0b9922dc68ea7db}

文字字串。 如果指定，它必須是&#x200B;**`ImageServing::catalog::id`**&#x200B;值、相對路徑（**`ImageServing::attribute::RootPath`**&#x200B;或&#x200B;**`ImageRendering::attribute::RootPath`**）或影像伺服器可訪問的影像檔案的絕對路徑。

## 預設 {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

從`default::ErrorImage`繼承（如果未定義）。 如果已定義錯誤，但為空，則即使已定義`default::ErrorImage`並返回HTTP錯誤狀態，錯誤影像行為也會被禁用。

## 另請參閱 {#section-3e0308eaf4124451909dacd570e27695}

[attribute::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f),  [attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3),  [catalog::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
