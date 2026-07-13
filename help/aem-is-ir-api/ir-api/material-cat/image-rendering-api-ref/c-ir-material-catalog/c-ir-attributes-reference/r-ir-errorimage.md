---
title: ErrorImage
description: 錯誤回應影像。 影像演算通常會在發生錯誤時傳回錯誤狀態，並顯示文字訊息。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ed48482f-79b0-4c81-b5cd-cf997f27d3ab
TQID: 'https://experienceleague.adobe.com/RRWlVPBpoUXafivRlOtzZoe5vExwnRB409SCOwhSRJI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 1%

---

# ErrorImage {#errorimage}

錯誤回應影像。 影像演算通常會在發生錯誤時傳回錯誤狀態，並顯示文字訊息。 `attribute::ErrorImage`允許設定發生錯誤時要傳回的影像。

發生錯誤時，伺服器會嘗試將`ImageRendering::attribute::ErrorImage`的值解譯為簡單的影像檔案路徑。 如果無法開啟檔案，則會將屬性值和錯誤詳細資料傳送至「影像伺服」，後者會依照`ImageServing::attribute::ErrorImage`中的說明進行處理。 如果「影像伺服」未傳回有效的回應影像，則會將標準HTTP錯誤狀態和文字訊息傳送給使用者端。

錯誤影像會傳回HTTP狀態200。

## 屬性 {#section-4a4a7e37ed11483db0b9922dc68ea7db}

文字字串。 如果已指定，它必須是&#x200B;**`ImageServing::catalog::id`**&#x200B;值、相對路徑（至&#x200B;**`ImageServing::attribute::RootPath`**&#x200B;或&#x200B;**`ImageRendering::attribute::RootPath`**），或影像伺服器可存取之影像檔案的絕對路徑。

## 預設 {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

如果未定義，則繼承自`default::ErrorImage`。 如果已定義但空白，即使已定義`default::ErrorImage`，也會停用錯誤影像行為，並傳回HTTP錯誤狀態。

## 另請參閱 {#section-3e0308eaf4124451909dacd570e27695}

[attribute：：DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)，[attribute：：ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b)，[attribute：：RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)，[catalog：：Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)

