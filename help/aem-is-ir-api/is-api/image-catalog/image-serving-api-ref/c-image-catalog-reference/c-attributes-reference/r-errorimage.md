---
description: 錯誤回應影像。 當發生錯誤時，影像伺服通常會傳回錯誤狀態及文字訊息。
seo-description: 錯誤回應影像。 當發生錯誤時，影像伺服通常會傳回錯誤狀態及文字訊息。
seo-title: ErrorImage
solution: Experience Manager
title: ErrorImage
topic: Scene7 Image Serving - Image Rendering API
uuid: b071c0cd-e7b8-422b-9b23-d93f504d9ce5
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# ErrorImage{#errorimage}

錯誤回應影像。 當發生錯誤時，影像伺服通常會傳回錯誤狀態及文字訊息。

`attribute::ErrorImage` 允許在發生錯誤時配置要返回的映像、目錄條目或模板。

>[!NOTE]
>
>也可以處理遺失的影像 `attribute::DefaultImage`。

可以設定「影像伺服」範本，將錯誤訊息文字轉譯至回應影像。 範本中可包含下列預先定義的變數 `$error.title` ，以簡短的錯誤說明取代， `$error.message`並以更詳細的錯誤說明取代(詳細程度已設定 `attribute::ErrorDetail`)。

如果錯誤影像／範本可以成功處理，則會傳回HTTP狀態200。 如果在此處理期間發生錯誤，則會傳回HTTP錯誤狀態和文字訊息。

## 屬性 {#section-f460c6c2dd1f46b29f9a79b093575f45}

文字字串。 如果指定，則必須是影像目錄中的有效目錄：:Id值，或是影像伺服器可存取之影像檔案的相對(對 `attribute::RootPath`)或絕對路徑。

## 預設 {#section-2885f289e5714ddca665a6aee401967f}

繼承自( `default::ErrorImage` 如果未定義)。 如果已定義但空白，則會停用錯誤影像行為，即使已 `default::ErrorImage` 定義，並傳回HTTP錯誤狀態和文字訊息。

## 範例 {#section-c92090abe1d247529542a8dd4960c2e6}

為了獲得包含錯誤資訊的響應影像，必須首先在影像目錄中定義模板。 在此案例中，我們會在影像目錄中建立一個名為 `onError`的項目，其中包含下列項目 `catalog::Modifier`:

`size=300,300&bgc=ffffff&text=$error.message$`

範本已註冊至 `attribute::ErrorImage`:

`ErrorImage=myCatalog/onError`

在此範例中，文字會使用預設字型、字型色彩和字型大小來轉換。

## 另請參閱 {#section-bbf1f85fc0a34033bdda1dd3e4e0bbb6}

[attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494) , [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md), attribute::DefaultImage [,](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)[attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561)
