---
description: 影像集資料。 提供一種機制，用於定義已排序的影像集和Dynamic Media查看器使用的控制屬性。
solution: Experience Manager
title: ImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: eacf0553-8cec-4a1d-80a5-6fe37b92b5bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 2%

---

# ImageSet{#imageset}

影像集資料。 提供一種機制，用於定義已排序的影像集和Dynamic Media查看器使用的控制屬性。

影像集由按逗號分隔的排序項清單組成，每個項由一個或多個子項（影像id、色板id、媒體檔案路徑、標籤等）組成，用分號和/或冒號分隔。

花括弧 `{ }` 括弧 `( )` 可用於限定某些內容（如顏色值）或指示嵌套集。 使用這種方法的大括弧或小括弧不得編碼，並且必須始終顯示為匹配對，否則將發生目錄分析錯誤。

>[!NOTE]
>
>以下字元用作集分隔符，當它們作為id或字串值的一部分出現在集中時，必須使用HTTP編碼：
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`



有關影像集的結構和使用的其他詳細資訊，請參閱「影像服務查看器」文檔。

伺服器返回此欄位的內容，但不會響應 `req=imageset` 請求。

## 標準集 {#section-5ecc8ffee7224668b63f601383665564}

影像服務本機支援以下集定義，對某些查看器的訪問涉及對集的伺服器端分析、驗證和處理。 通過在中指定相應的值，可以識別每個設定類型 `catalog::AssetType`。

**基本色板集**

基本色板集中的每個項包括對影像記錄的引用和對用作色板的影像記錄的可選單獨引用。

| `*`basicSwatchSet`*` | `*`色板項`*&#42;[',' *`色板項`*]` |
|---|---|
| `*`色板項`*` | `*`影像ID`*[';' *`樣本`*]` |
| `*`樣本`*` | `*`色板ID`*|solidColorSpecifier` |
| `*`影像ID`*` | IS映像引用（目錄/ID） |
| `*`色板ID`*` | IS映像引用（目錄/ID） |
| `*`solidColor說明符`*` | ` '{0x' *`拉格布`* [ *`標籤`*]'}'` |
| `*`拉格布`*` | 固色色板的6位十六進位RGB色值 |
| `*`label`*` | 實色色板的可選文本標籤 |

**層次色板集**

分層色板集中的每個項都可以由基本色板項或對色板集記錄的引用組成（此類項需要色板）。

| `*`層次色板集`*` | `*`hierarchicalSwatchItem`* &#42;[ ',' *`hierarchicalSwatchItem`* ]` |
|---|---|
| `*`hierarchicalSwatchItem`*` | `*`色板項`* | { *`basicSwatchSetId`* ';' *`樣本`* }` |
| `*`basicSwatchSetId`*` | 對定義基本色板集的目錄記錄的IS引用（目錄/ID） |

**基本旋轉集**

基本旋轉集由簡單的影像ID清單組成。

*`basicSpinSet imageId`*  &#42;`[ ';'`  *`imageId`* `]`

**二維自旋集**

二維旋轉集中的每個項目都可以由簡單影像、對基本旋轉集的引用或由大括弧分隔的串聯基本旋轉集組成。 可以使用圓括弧而不是花括弧。

| `*`2dSpinItem`*` | `*`2d旋轉集`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| `*`2dSpinItem`*` | `*`影像ID`* | { '{' *`basicSpinSet`* '}' } | *`basicSpinSetId`*` |
| `*`basicSpinSetId`*` | IS對定義基本旋轉集的目錄記錄的引用 |

**頁面集**

頁面集中的每個項目最多可以包含三個用冒號分隔的頁面影像。

| `*`頁集`*` | `*`pageItem`* &#42;[ , *`pageItem`* ]` |
|---|---|
| `*`pageItem`*` | `*`影像ID`* [ : *`影像ID`* [ : *`影像ID`* ] ]` |

**媒體集**

媒體集中的每個項目都可以包括影像、基本色板集、分層色板集、基本旋轉集、二維旋轉集、頁集或視頻資產。 每個媒體集項目也可以包含可選色板和類型標識符。

| `*`媒體集`*` | `*`物料`* &#42;[ , *`物料`* ]` |
|---|---|
| `*`項目`*` | ` { *`視頻項`* | *`recutItem`* | *`imageItem`*}} | *`setItem`* } [ ; [ *`ID`* ] [ ; [ *`保留`* ] ] ]` |
| `*`視頻項`*` | `*`視頻`* ; *`色板ID`*` |
| `*`recutItem`*` | `*`斜`* ; *`色板ID`*` |
| `*`imageItem`*` | `*`影像ID`* ; [ *`色板ID`* ]` |
| `*`setItem`*` | ` { *`集ID`* | { '{' *`內聯集`* '}' } } ; *`色板ID`*` |
| `*`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| `*`色板ID`*` | IS映像ID |
| `*`視頻`*` | 視頻/動畫檔案路徑或靜態目錄ID |
| `*`斜`*` | 重新定義XML檔案路徑或靜態目錄ID |
| `*`影像ID`*` | IS映像ID |
| `*`集ID`*` | IS對影像、旋轉或對錄集的引用 |
| `*`內聯集`*` | 內嵌影像、旋轉或對錄集 |
| `*`已保留`*` | 保留供將來使用 |

**Video Sets**

視頻集由視頻ID的簡單清單組成，其中每個ID引用靜態內容目錄中的條目。

*`videoSet videoId`*  &#42;`[ ,`  *`videoId`* `]`

## 屬性 {#section-17c731e5c46646aa90ac21f39bb693ca}

文本字串。 以逗號分隔的清單 `catalog::Id` 值、絕對影像伺服器檔案路徑或相對於 `attribute::RootPath`。 同一影像在集合中可被引用多次。 定義目錄記錄可能出現在任何位置的集中。

此欄位參與文本字串本地化。 除 *`label`* 字串( *`solidColorSpecifier`*)如果所有分隔欄位至少包含一個「 」，則這些欄位都會本地化 `^loc=…^`&#39;本地化標籤。 請參閱 [文本字串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) 的 *HTTP協定引用* 的雙曲餘切值。

## 預設 {#section-c3a60e360393478284f0f2d2da5b963b}

無。

## 請亦參閱 {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) 。 [屬性：:RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)。 [對象ID轉換](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) 。 [文本字串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) ，影像服務查看器文檔
