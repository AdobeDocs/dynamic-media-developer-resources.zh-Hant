---
description: 預設影像檔案尾碼。 如果路徑不包含檔案尾碼，則附加到目錄路徑（或目錄掩碼路徑）欄位值
solution: Experience Manager
title: DefaultExt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 43b3e5b8-6374-458d-8503-8e04c8c84233
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---

# DefaultExt{#defaultext}

預設影像檔案尾碼。 如果路徑不包含檔案尾碼，則附加至目錄：:Path（或catalog::MaskPath）欄位值

檔案尾碼由句號和字串的句號和結尾之間的一個或多個字元組成。 如果路徑未解析為目錄項，且如果最後一個路徑元素不包含檔案尾碼，尾碼會附加至http路徑。

## 屬性 {#section-b024e6450b414ccc8b83a48a3b4e00f9}

文字字串。 必須包含前導「。」 和一個或多個字元。

## 預設 {#section-1194c36ffe0748c5b9ff7d732a506588}

若未定義，則繼承自`default::DefaultExt`。 如果已定義但為空，則使用此目錄時不會將預設尾碼套用至影像名稱。

## 另請參閱 {#section-d7c408b979844643adff8258f500eb7c}

[目錄：:Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ，目 [錄：::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)
