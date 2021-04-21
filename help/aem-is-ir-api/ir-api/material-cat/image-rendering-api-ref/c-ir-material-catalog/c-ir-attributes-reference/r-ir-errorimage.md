---
description: 錯誤回應影像。 當發生錯誤時，「影像演算」通常會傳回錯誤狀態並顯示文字訊息。 attribute ErrorImage允許在發生錯誤時配置要返回的映像。
solution: Experience Manager
title: ErrorImage *
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 1%

---


# ErrorImage *{#errorimage}

錯誤回應影像。 當發生錯誤時，「影像演算」通常會傳回錯誤狀態並顯示文字訊息。 attribute::ErrorImage允許在發生錯誤時配置要返回的映像。

發生錯誤時，伺服器首先嘗試將`ImageRendering::attribute::ErrorImage`的值解譯為簡單的映像檔案路徑。 如果無法開啟檔案，則會傳送屬性值和錯誤詳細資訊給影像伺服，影像伺服會依`ImageServing::attribute::ErrorImage`所述進行處理。 如果「影像伺服」未傳回有效的回應影像，則會傳送標準HTTP錯誤狀態和文字訊息給用戶端。

以HTTP狀態200傳回錯誤影像。

## 屬性 {#section-4a4a7e37ed11483db0b9922dc68ea7db}

文字字串。 如果指定，它必須是&#x200B;**`ImageServing::catalog::id`**&#x200B;值、**`ImageServing::attribute::RootPath`**&#x200B;或&#x200B;**`ImageRendering::attribute::RootPath`**&#x200B;的相對路徑，或是影像伺服器可存取之影像檔案的絕對路徑。

## 預設 {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

如果未定義，則繼承自`default::ErrorImage`。 如果已定義但為空，則會禁用錯誤映像行為，即使已定義`default::ErrorImage` ，並返回HTTP錯誤狀態。

## 另請參閱 {#section-3e0308eaf4124451909dacd570e27695}

[attribute::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f),  [attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3),  [catalog::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
