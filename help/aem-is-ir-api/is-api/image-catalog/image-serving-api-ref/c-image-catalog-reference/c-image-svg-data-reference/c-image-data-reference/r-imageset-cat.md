---
description: 影像集資料。 提供一種機制，可定義已排序的影像集並控制Dynamic Media檢視器使用的屬性。
solution: Experience Manager
title: ImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 2%

---


# 影像集{#imageset}

影像集資料。 提供一種機制，可定義已排序的影像集並控制Dynamic Media檢視器使用的屬性。

影像集由排序的、以逗號分隔的項目清單組成，每個項目由一個或多個子項目（影像ID、色票ID、媒體檔案路徑、標籤等）組成，由分號和／或冒號分隔。

大括弧`{ }`和括弧`( )`可用於分隔某些內容（如顏色值）或表示嵌套集。 此方式使用的大括弧或括弧不得進行編碼，而且必須始終顯示為匹配的對，否則將發生目錄解析錯誤。

>[!NOTE]
>
>下列字元用作設定分隔字元，且當這些字元在設定中顯示為id或字串值時，必須使用HTTP編碼：
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`



請參閱影像伺服檢視器檔案，以取得有關影像集結構與使用的其他詳細資訊。

伺服器會回應`req=imageset`要求而傳回此欄位的內容，但不會進行修改。

## 標準集{#section-5ecc8ffee7224668b63f601383665564}

「影像伺服」原本支援下列設定定義，而存取特定檢視器時需要伺服器端剖析、驗證和處理設定。 每個設定類型都可通過在`catalog::AssetType`中指定相應值來標識。

**基本色票集**

基本色票集中的每個項目都包括對影像記錄的引用和對用作色票的影像記錄的可選單獨引用。

| `*`basicSwatchSet`*` | `*`SwatchItemswatchItem`*&#42;[',' *``*]` |
|---|---|
| `*`swatchItem`*` | `*`imageIdswatch`*[';' *``*]` |
| `*`色票`*` | `*`swatchId`*|solidColorSpecifier` |
| `*`imageId`*` | IS影像參考（目錄/ID） |
| `*`swatchId`*` | IS影像參考（目錄/ID） |
| `*`solidColorSpecifier`*` | ` '{0x' *``* [ *`Rrggbblabel`*]'}'` |
| `*`rggbb`*` | 固色色票的6位數十六進位RGB色彩值 |
| `*`label`*` | 純色色票的可選文字標籤 |

**階層色票集**

階層式色票集中的每個項目都可由基本色票項目或對色票集記錄的參考（此類項目需要色票）組成。

| `*`hierarchicalSwatchSet`*` | `*`hierarchicalSwatchItemhieralSwatchItem`* &#42;[ ',' *``* ]` |
|---|---|
| `*`hierarchicalSwatchItem`*` | `*`SwatchIntembasicSwatchSetIdswatch`* | { *``* ';' *``* }` |
| `*`basicSwatchSetId`*` | 定義基本色票集的目錄記錄的IS參考（目錄/ID） |

**基本回轉集**

基本回轉集由簡單的影像ID清單組成。

*`basicSpinSet imageId`*  *`[ ';'`  *`imageId`* `]`

**二維自旋集**

二維回轉集中的每個項目都可由簡單影像、基本回轉集的參考，或由大括弧分隔的內嵌基本回轉集組成。 可以使用括弧來取代大括弧。

| `*`2dSpinItem`*` | `*`2dSpinSet`* *` 2dSpinItem`* &#42;[ ',' *` 2dSpinItem`* ]` |
|---|---|
| `*`2dSpinItem`*` | `*``* | { '{' *``* '}' } | *`imageIdbasicSpinSetbasicSpinSetId`*` |
| `*`basicSpinSetId`*` | 定義基本回轉集的目錄記錄的IS參考（目錄/ID） |

**頁面集**

頁面集中的每個項目最多可以由三個以冒號分隔的頁面影像組成。

| `*`pageSet`*` | `*`pageItempageItem`* &#42;[ , *``* ]` |
|---|---|
| `*`pageItem`*` | `*`imageIdimageImageId`* [ : *``* [ : *``* ] ]` |

**媒體集**

媒體集中的每個項目都可由影像、基本色票集、階層式色票集、基本回轉集、二維回轉集、頁面集或視訊資產組成。 每個媒體集項目也可以包含選用的色票和文字識別碼。

| `*`mediaSet`*` | `*`itemitem`* &#42;[ , *``* ]` |
|---|---|
| `*`項目`*` | ` { *``* | *``* | *``*}} | *``* } [ ; [ *``* ] [ ; [ *`videoItemrecutItemimageItemsetItemIDreserved`* ] ] ]` |
| `*`videoItem`*` | `*``* ; *`videoswatchId`*` |
| `*`recutItem`*` | `*``* ; *`recutswatchId`*` |
| `*`imageItem`*` | `*`imageIdswatchId`* ; [ *``* ]` |
| `*`setItem`*` | ` { *``* | { '{' *``* '}' } } ; *`setIdinlineSetswatchId`*` |
| `*`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| `*`swatchId`*` | IS影像ID |
| `*`視訊`*` | 視訊／動畫檔案路徑或靜態目錄ID |
| `*`recut`*` | 重新剪輯定義XML檔案路徑或靜態目錄ID |
| `*`imageId`*` | IS影像ID |
| `*`setId`*` | IS對影像、回轉或加對錄集的引用 |
| `*`inlineSet`*` | 內嵌影像、回轉或加對錄集 |
| `*`已保留`*` | 留待日後使用 |

**Video Sets**

視訊集由視訊ID的簡單清單組成，其中每個ID都參照靜態內容目錄中的項目。

*`videoSet videoId`*  *`[ ,`  *`videoId`* `]`

## 屬性 {#section-17c731e5c46646aa90ac21f39bb693ca}

文字字串。 以逗號分隔的`catalog::Id`值、絕對影像伺服器檔案路徑或相對於`attribute::RootPath`的檔案路徑清單。 在集合中可以多次引用同一影像。 定義目錄記錄可以出現在集合中的任意位置。

此欄位參與文字字串本地化。 除了&#x200B;*`label`*&#x200B;字串（*`solidColorSpecifier`*&#x200B;的一部分）外，如果所有分隔欄位包含至少一個&#39; `^loc=…^`&#39;本地化Token，則這些欄位都會本地化。 如需詳細資訊，請參閱&#x200B;*HTTP通訊協定參考*&#x200B;中的[文字字串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)。

## 預設 {#section-c3a60e360393478284f0f2d2da5b963b}

無。

## 請亦參閱 {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) ，屬 [性：:RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)，物 [件ID轉換](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) ，文字字串本 [地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) ，影像伺服檢視器檔案
