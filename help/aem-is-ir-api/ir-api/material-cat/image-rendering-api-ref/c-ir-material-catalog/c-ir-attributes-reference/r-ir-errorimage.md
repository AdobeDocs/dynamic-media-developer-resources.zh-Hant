---
title: 錯誤影像
description: 錯誤響應影像。 當出現錯誤時，影像呈現通常會返回帶有文本消息的錯誤狀態。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ed48482f-79b0-4c81-b5cd-cf997f27d3ab
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 1%

---

# 錯誤影像 {#errorimage}

錯誤響應影像。 當出現錯誤時，影像呈現通常會返回帶有文本消息的錯誤狀態。 的 `attribute::ErrorImage` 允許在出現錯誤時配置要返回的映像。

發生錯誤時，伺服器會嘗試解釋 `ImageRendering::attribute::ErrorImage`作為簡單的影像檔案路徑。 如果無法開啟檔案，則會將屬性值和錯誤詳細資訊發送到Image Serving，該Image Serving將按照中所述進行處理 `ImageServing::attribute::ErrorImage`。 如果Image Serving未返回有效的響應映像，則標準HTTP錯誤狀態和文本消息將發送到客戶端。

返回錯誤影像，HTTP狀態為200。

## 屬性 {#section-4a4a7e37ed11483db0b9922dc68ea7db}

文本字串。 如果指定，則必須是 **`ImageServing::catalog::id`** 值，相對路徑(到 **`ImageServing::attribute::RootPath`** 或 **`ImageRendering::attribute::RootPath`**)，或映像伺服器可訪問的映像檔案的絕對路徑。

## 預設 {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

繼承自 `default::ErrorImage` 的子菜單。 如果已定義但為空，則會禁用錯誤影像行為，即使 `default::ErrorImage` 定義，並返回HTTP錯誤狀態。

## 另請參閱 {#section-3e0308eaf4124451909dacd570e27695}

[屬性：:DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)。 [屬性：:ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b)。 [屬性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)。 [目錄：:ID](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
