---
description: 錯誤響應影像。 當出現錯誤時，Image Serving通常返回帶有文本消息的錯誤狀態。
solution: Experience Manager
title: 錯誤影像
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f412a379-525e-42fc-97bf-b10e00da6a20
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---

# 錯誤影像{#errorimage}

錯誤響應影像。 當出現錯誤時，Image Serving通常返回帶有文本消息的錯誤狀態。

`attribute::ErrorImage` 允許在出錯時配置要返回的映像、目錄條目或模板。

>[!NOTE]
>
>也可以使用 `attribute::DefaultImage`。

可以配置「影像服務」模板，該模板可能會將錯誤消息文本呈現到響應影像中。 以下預定義變數可包含在 `$error.title` 模板，用簡短的錯誤說明替換，和 `$error.message`，用更詳細的錯誤說明替換(詳細級別配置為 `attribute::ErrorDetail`)。

如果錯誤映像/模板可以成功處理，則返回HTTP狀態200。 如果在此處理過程中出現錯誤，則返回HTTP錯誤狀態和文本消息。

## 屬性 {#section-f460c6c2dd1f46b29f9a79b093575f45}

文本字串。 如果指定，則必須是影像目錄中的有效目錄：:Id值或相對(至 `attribute::RootPath`)或映像伺服器可訪問的映像檔案的絕對路徑。

## 預設 {#section-2885f289e5714ddca665a6aee401967f}

繼承自 `default::ErrorImage` 的子菜單。 如果已定義但為空，則會禁用錯誤影像行為，即使 `default::ErrorImage` 定義，並返回HTTP錯誤狀態和文本消息。

## 範例 {#section-c92090abe1d247529542a8dd4960c2e6}

要獲取包含錯誤資訊的響應影像，必須先在影像目錄中定義模板。 在這種情況下，我們會在映像目錄中建立一個名為 `onError`，包含以下內容 `catalog::Modifier`:

`size=300,300&bgc=ffffff&text=$error.message$`

模板已註冊 `attribute::ErrorImage`:

`ErrorImage=myCatalog/onError`

在此示例中，使用預設字型、字型顏色和字型大小來呈現文本。

## 另請參閱 {#section-bbf1f85fc0a34033bdda1dd3e4e0bbb6}

[屬性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494) 。 [目錄：:ID](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)。 [屬性：:DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)。 [屬性：:ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561)
