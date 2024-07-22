---
description: 影像集資料。 提供可定義Dynamic Media檢視器使用的已排序影像集和控制屬性集的機制。
solution: Experience Manager
title: ImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: eacf0553-8cec-4a1d-80a5-6fe37b92b5bf
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 1%

---

# ImageSet{#imageset}

影像集資料。 提供可定義Dynamic Media檢視器使用的已排序影像集和控制屬性集的機制。

影像集包含以逗號分隔的已排序專案清單。 每個專案都包含一或多個子專案（影像ID、色票ID、媒體檔案路徑、標籤等），並以分號或冒號分隔，或同時包含兩者。

大括弧`{ }`和括弧`( )`可用來分隔某些內容（例如色彩值）或表示巢狀集合。 以此方式使用的大括弧或括弧不得編碼，且必須一律顯示為相符配對，否則會發生目錄剖析錯誤。

>[!NOTE]
>
>下列字元會當作設定分隔字元，而且當這些字元出現在設定中做為id或字串值的一部分時，必須以HTTP編碼：
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`


如需有關影像集的結構和使用的更多詳細資訊，請參閱「影像伺服檢視器」檔案。

伺服器會傳回此欄位的內容，但不修改以回應`req=imageset`要求。

## 標準集 {#section-5ecc8ffee7224668b63f601383665564}

「影像伺服」原生支援下列集合定義，且特定檢視器的存取包含伺服器端剖析、驗證及處理集合。 在`catalog::AssetType`中指定對應的值，即可識別每個集合型別。

**基本色票集**

基本色票集的每個專案都包含影像記錄的參照，以及作為色票使用的影像記錄的選擇性個別參照。

| `*`basicSwatchSet`*` | `*`swatchItem`*&#42;[',' *`swatchItem`*]` |
|---|---|
| `*`色票專案`*` | `*`imageId`*[';' *`色票`*]` |
| `*`色票`*` | `*`色票識別碼`*|solidColorSpecifier` |
| `*`imageId`*` | IS影像參考（目錄/ID） |
| `*`色票識別碼`*` | IS影像參考（目錄/ID） |
| `*`solidColorSpecificer`*` | ` '{0x' *`rrggbb`* [ *`標籤`*]'}'` |
| `*`rrggbb`*` | 純色色票的包裝6位數十六進位RGB色彩值 |
| `*`標籤`*` | 純色色票的可選文字標籤 |

**階層式色票集**

階層式色票集中的每個專案都可以包含基本色票專案或色票集記錄的參考（這類專案需要色票）。

| `*`hierarchicalSwatchSet`*` | `*`hierarchicalSwatchItem`* &#42;[ ',' *`hierarchicalSwatchItem`* ]` |
|---|---|
| `*`hierarchicalSwatchItem`*` | `*`色票專案`* | { *`basicSwatchSetId`* ';' *`色票`* }` |
| `*`basicSwatchSetId`*` | 定義基本色票集的目錄記錄的IS參考（目錄/ID） |

**基本迴轉集**

基本迴轉集是由影像ID的簡單清單所組成。

*`basicSpinSet imageId`*  &#42;`[ ';'`  *`imageId`* `]`

**二維迴轉集**

二維迴轉集的每個專案都可以包含簡單影像、基本迴轉集的參照或以大括弧分隔的內嵌基本迴轉集。 可使用括弧取代大括弧。

| `*`2dSpinItem`*` | `*`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| `*`2dSpinItem`*` | `*`imageId`* | { '{' *`basicSpinSet`* '}' } | *`basicSpinSetId`*` |
| `*`basicSpinSetId`*` | 定義基本迴轉集的目錄記錄的IS參考（目錄/ID） |

**頁面集**

頁面集中的每個專案最多可包含以冒號分隔的三頁影像。

| `*`pageSet`*` | `*`pageItem`* &#42;[ , *`pageItem`* ]` |
|---|---|
| `*`pageItem`*` | `*`imageId`* [ : *`imageId`* [ : *`imageId`* ] ]` |

**媒體集**

媒體集中的每個專案都可以包含影像、基本色票集、階層式色票集、基本迴轉集、二維迴轉集、頁面集或視訊資產。 每個媒體集專案也可以包含選用的色票和型別識別碼。

| `*`媒體集`*` | `*`專案`* &#42;[ , *`專案`* ]` |
|---|---|
| `*`專案`*` | ` { *`videoItem`* | *`recutItem`* | *`imageItem`*}} | *`setItem`* } [ ; [ *`ID`* ] [ ; [ *`保留`* ] ] ]` |
| `*`videoItem`*` | `*`視訊`* ; *`色票識別碼`*` |
| `*`recutItem`*` | `*`重新剪輯`* ; *`色票識別碼`*` |
| `*`imageItem`*` | `*`imageId`* ; [ *`swatchId`* ]` |
| `*`setItem`*` | ` { *`setId`* | { '{' *`inlineSet`* '}' } } ; *`swatchId`*` |
| `*`識別碼`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| `*`色票識別碼`*` | 是影像ID |
| `*`影片`*` | 視訊/動畫檔案路徑或靜態目錄ID |
| `*`重新剪輯`*` | 重新剪輯定義XML檔案路徑或靜態目錄ID |
| `*`imageId`*` | 是影像ID |
| `*`setId`*` | IS對影像、迴轉或eCatalog集的參照 |
| `*`inlineSet`*` | 內嵌影像、迴轉或ecatalog集 |
| `*`保留`*` | 保留供未來使用 |

**Video Sets**

視訊集由簡單的視訊ID清單組成，其中每個ID都參考靜態內容目錄中的專案。

*`videoSet videoId`*  &#42;`[ ,`  *`videoId`* `]`

## 屬性 {#section-17c731e5c46646aa90ac21f39bb693ca}

文字字串。 以逗號分隔的`catalog::Id`值清單、絕對影像伺服器檔案路徑，或相對於`attribute::RootPath`的檔案路徑。 同一個影像在集中可能會被參考多次。 定義目錄記錄可出現在集合的任何位置。

此欄位參與文字字串本地化。 除了&#x200B;*`label`*&#x200B;字串（*`solidColorSpecifier`*&#x200B;的一部分）之外，如果分隔欄位至少包含一個&#39; `^loc=…^`&#39;本地化Token，則所有欄位都會本地化。 如需詳細資訊，請參閱&#x200B;*HTTP通訊協定參考*&#x200B;中的[文字字串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)。

## 預設 {#section-c3a60e360393478284f0f2d2da5b963b}

無。

## 請亦參閱 {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) ， [attribute：：RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)， [物件識別碼轉譯](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) ， [文字字串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) ，影像伺服檢視器檔案
