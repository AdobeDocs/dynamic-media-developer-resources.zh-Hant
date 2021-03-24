---
description: 預設影像檔案字尾。 如果路徑不包含檔案尾碼，則附加到目錄路徑（或目錄掩碼路徑）欄位值
solution: Experience Manager
title: DefaultExt
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 2%

---


# DefaultExt{#defaultext}

預設影像檔案字尾。 附加至目錄：:Path（或目錄：:MaskPath）欄位值（如果路徑不包含檔案尾碼）

檔案尾碼由句點和字串的句點和結尾之間的一個或多個字元組成。 如果路徑未解析為目錄條目，並且最後一個路徑元素不包含檔案尾碼，則尾碼會附加到http路徑。

## 屬性 {#section-b024e6450b414ccc8b83a48a3b4e00f9}

文字字串。 必須包含前導&#39;.&#39;。 和一或多個角色。

## 預設 {#section-1194c36ffe0748c5b9ff7d732a506588}

如果未定義，則繼承自`default::DefaultExt`。 如果已定義但空白，則使用此目錄時不會將預設字尾套用至影像名稱。

## 另請參閱 {#section-d7c408b979844643adff8258f500eb7c}

[目錄：:Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ，目 [錄：:MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)
