---
description: 錯誤響應影像。 影像伺服通常會在發生錯誤時，傳回帶有文字訊息的錯誤狀態。
solution: Experience Manager
title: ErrorImage
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: f412a379-525e-42fc-97bf-b10e00da6a20
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 1%

---

# ErrorImage{#errorimage}

錯誤響應影像。 影像伺服通常會在發生錯誤時，傳回帶有文字訊息的錯誤狀態。

`attribute::ErrorImage` 允許配置在發生錯誤時要返回的影像、目錄條目或模板。

>[!NOTE]
>
>`attribute::DefaultImage`也可處理遺失的影像。

可以設定「影像伺服」範本，將錯誤訊息文字轉譯至回應影像中。 `$error.title`範本中可包含下列預先定義的變數，這些變數會以短錯誤說明取代； `$error.message`則以更詳細的錯誤說明取代（詳細程度會以`attribute::ErrorDetail`設定）。

如果錯誤影像/範本可成功處理，則會傳回HTTP狀態200。 如果此處理期間發生錯誤，則會傳回HTTP錯誤狀態和文字訊息。

## 屬性 {#section-f460c6c2dd1f46b29f9a79b093575f45}

文字字串。 如果指定，則必須是影像目錄中的有效目錄：:Id值，或是影像伺服器可訪問的影像檔案的相對路徑(`attribute::RootPath`)或絕對路徑。

## 預設 {#section-2885f289e5714ddca665a6aee401967f}

若未定義，則繼承自`default::ErrorImage`。 如果已定義但為空，則即使已定義`default::ErrorImage`，並返回HTTP錯誤狀態和文本消息，錯誤影像行為也會被禁用。

## 範例 {#section-c92090abe1d247529542a8dd4960c2e6}

要獲取包含已呈現到影像中的錯誤消息的響應影像，必須首先在影像目錄中定義模板。 在此情況下，我們會在影像目錄中建立名為`onError`的項目，並在`catalog::Modifier`中包含下列項目：

`size=300,300&bgc=ffffff&text=$error.message$`

模板已用`attribute::ErrorImage`註冊：

`ErrorImage=myCatalog/onError`

在此示例中，將使用預設字型、字型顏色和字型大小來呈現文本。

## 另請參閱 {#section-bbf1f85fc0a34033bdda1dd3e4e0bbb6}

[attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494) ,  [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md),  [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561)
