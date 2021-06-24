---
description: 影像集資料。 提供定義已排序影像集和Dynamic Media檢視器所使用控制屬性的機制。
solution: Experience Manager
title: ImageSet
feature: Dynamic Media Classic, SDK/API，影像集
role: Developer,Business Practitioner
exl-id: eacf0553-8cec-4a1d-80a5-6fe37b92b5bf
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 2%

---

# ImageSet{#imageset}

影像集資料。 提供定義已排序影像集和Dynamic Media檢視器所使用控制屬性的機制。

影像集由以逗號分隔的排序項目清單組成，每個項目都由一個或多個子項目（影像ID、色票ID、媒體檔案路徑、標籤等）組成，由分號和/或冒號分隔。

大括弧`{ }`和括弧`( )`可用於分隔某些內容（如顏色值）或指示嵌套集。 此方式使用的大括弧或括弧不得編碼，且必須始終顯示為匹配對，否則將發生目錄解析錯誤。

>[!NOTE]
>
>下列字元會作為設定分隔字元，且在設定中顯示為id或字串值時，必須進行HTTP編碼：
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`



有關影像集的結構和使用的其他詳細資訊，請參閱影像伺服檢視器檔案。

伺服器會回傳此欄位的內容，而不會因應`req=imageset`要求而進行修改。

## 標準集 {#section-5ecc8ffee7224668b63f601383665564}

影像伺服器原本支援下列集合定義，而透過特定檢視器存取涉及該集合的伺服器端剖析、驗證和處理。 可通過在`catalog::AssetType`中指定相應值來標識每個設定類型。

**基本色票集**

基本色票集中的每個項目都包含對影像記錄的引用和對用作色票的影像記錄的可選單獨引用。

| `*`basicSwatchSet`*` | `*``*&#42;[',' *`swatchItemswatchItem`*]` |
|---|---|
| `*`swatchItem`*` | `*``*[';' *`imageIdswatch`*]` |
| `*`色票`*` | `*`swatchId`*|solidColorSpecifier` |
| `*`imageId`*` | IS影像參考（目錄/id） |
| `*`swatchId`*` | IS影像參考（目錄/id） |
| `*`solidColorSpecifier`*` | ` '{0x' *``* [ *`rrggbblabel`*]'}'` |
| `*`rggbb`*` | 固色色票的6位數十六進位RGB色彩值 |
| `*`label`*` | 實色色板的可選文本標籤 |

**階層色票集**

層次色板集中的每個項目都可由基本色板項目或對色板集記錄的引用組成（此類項目需要色板）。

| `*`hierarchicalSwatchSet`*` | `*``* &#42;[ ',' *`hierarchicalSwatchItemhierarcialSwatchItem`* ]` |
|---|---|
| `*`hierarchicalSwatchItem`*` | `*``* | { *``* ';' *`swatchItembasicSwatchSetIdswatch`* }` |
| `*`basicSwatchSetId`*` | 對定義基本色票集的目錄記錄的IS引用（目錄/ID） |

**基本回轉集**

基本回轉集包含簡單的影像ID清單。

*`basicSpinSet imageId`*  *`[ ';'`  *`imageId`* `]`

**二維回轉集**

二維回轉集中的每個項目都可由簡單影像、基本回轉集的參照，或由大括弧分隔的內線基本回轉集組成。 可使用括弧而非大括弧。

| `*`2dSpinItem`*` | `*`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| `*`2dSpinItem`*` | `*``* | { '{' *``* '}' } | *`imageIdbasicSpinSetbasicSpinSetId`*` |
| `*`basicSpinSetId`*` | 對定義基本回轉集的目錄記錄進行IS引用（目錄/ID） |

**頁面集**

頁面集中的每個項目最多可包含三個以冒號分隔的頁面影像。

| `*`pageSet`*` | `*``* &#42;[ , *`pageItempageItem`* ]` |
|---|---|
| `*`pageItem`*` | `*``* [ : *``* [ : *`imageIdimageIdimageId`* ] ]` |

**媒體集**

媒體集中的每個項目都可包含影像、基本色票集、階層色票集、基本回轉集、二維回轉集、頁面集或視訊資產。 每個媒體集項目也可包含選用的色票和類型識別碼。

| `*`mediaSet`*` | `*``* &#42;[ , *`itemitem`* ]` |
|---|---|
| `*`項目`*` | ` { *``* | *``* | *``*}} | *``* } [ ; [ *``* ] [ ; [ *`videoItemrecutItemimageItemsetItemIDreserved`* ] ] ]` |
| `*`videoItem`*` | `*``* ; *`videoswatchId`*` |
| `*`recutItem`*` | `*``* ; *`recutswatchId`*` |
| `*`imageItem`*` | `*``* ; [ *`imageIdswatchId`* ]` |
| `*`setItem`*` | ` { *``* | { '{' *``* '}' } } ; *`setIdinlineSetswatchId`*` |
| `*`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| `*`swatchId`*` | IS影像ID |
| `*`影片`*` | 視頻/動畫檔案路徑或靜態目錄ID |
| `*`重設`*` | 重新定義XML檔案路徑或靜態目錄ID |
| `*`imageId`*` | IS影像ID |
| `*`setId`*` | 是影像、回轉或對話集的參考 |
| `*`inlineSet`*` | 內嵌的影像、回轉或對話集 |
| `*`已保留`*` | 保留供將來使用 |

**Video Sets**

視訊集由簡單的視訊ID清單組成，每個ID會參照靜態內容目錄中的項目。

*`videoSet videoId`*  *`[ ,`  *`videoId`* `]`

## 屬性 {#section-17c731e5c46646aa90ac21f39bb693ca}

文字字串。 `catalog::Id`值、絕對影像伺服器檔案路徑或相對於`attribute::RootPath`的檔案路徑的逗號分隔清單。 在集合中可以參照相同影像多次。 定義目錄記錄可能出現在任何位置的集合中。

此欄位參與文字字串本地化。 除了&#x200B;*`label`*&#x200B;字串（*`solidColorSpecifier`*&#x200B;的一部分）之外，如果所有分隔欄位至少包含一個「 `^loc=…^`」本地化代號，則這些欄位都會本地化。 如需詳細資訊，請參閱&#x200B;*HTTP通訊協定參考*&#x200B;中的[文字字串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)。

## 預設 {#section-c3a60e360393478284f0f2d2da5b963b}

無。

## 請亦參閱 {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) ,  [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md),  [Object Id翻譯](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) ,  [Text String Localization](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) , Image Serving Viewers Documentation
