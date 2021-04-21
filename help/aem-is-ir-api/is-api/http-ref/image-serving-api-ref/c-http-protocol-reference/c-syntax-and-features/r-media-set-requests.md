---
description: 「影像伺服」提供擷取階層文字回應（xml或json）的機制，此回應代表與特定記錄的目錄ImageSet相關的所有資源和中繼資料。
solution: Experience Manager
title: 媒體集請求
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%

---


# 媒體集請求{#media-set-requests}

「影像伺服」提供擷取階層文字回應（xml或json）的機制，此回應代表與目錄：:ImageSet特定記錄相關的所有資源和中繼資料。

檢視器可使用此機制產生回應，以通知簡單影像、視訊、視訊集、色票集、回轉集、頁面集(e-catalog)和媒體集的簡報。

## 請求語法{#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

使用`req=set`修飾詞並參考淨路徑中的目錄記錄ID，可以檢索`catalog::ImageSet`的設定響應。 或者，您也可以使用`imageset=`修飾元，直接在URL中指定影像集。 如果使用`imageset=`修飾元來指定影像集，則整個值應以大括弧括住，以逸出影像集值，並確保所包含的修飾元不會解讀為URL查詢字串的一部分。

## 集合響應類型{#section-93eb0a1f70344da2a888e56372ad3896}

set機制支援以下類型的響應：

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>簡單影像 </p></td> 
  <td class="stentry"> <p>未定義<span class="codeph">目錄的影像記錄：:ImageSet</span>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>簡單影片 </p></td> 
  <td class="stentry"> <p>靜態內容目錄中的視訊記錄。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>色票集 </p></td> 
  <td class="stentry"> <p>一組項目，包括對影像記錄的引用和對用作色票的影像記錄的可選單獨引用。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>層次色票集 </p></td> 
  <td class="stentry"> <p>一組由基本色票項目或對色票集記錄的引用組成的項目。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>回轉集 </p></td> 
  <td class="stentry"> <p>一組項目，由簡單的影像ID清單組成。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>二維自旋集 </p></td> 
  <td class="stentry"> <p>一組由簡單影像或基本旋轉集的引用組成的項目。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>頁集 </p></td> 
  <td class="stentry"> <p>一組項目，包含最多3張頁面影像的清單 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>媒體集 </p></td> 
  <td class="stentry"> <p>一組項目，包括簡單影像、視訊集、色票集、階層式色票集、回轉集、二維回轉集、頁面集和視訊資產。 每個媒體集項目也可以包含一個可選色票。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>影片集 </p></td> 
  <td class="stentry"> <p>一組由簡單影片清單組成的項目。 </p></td> 
 </tr> 
</table>

## 外部設定類型檢測{#section-3dd6e453528d46898e559d31458a59ba}

當接收到`req=set`請求時，由`catalog::AssetType`的值確定要生成的響應類型。 如果未定義`catalog::AssetType`，則響應類型由以下規則確定：

* 如果在映像目錄中找到記錄，則定義`catalog::ImageSet`

   * 如果記錄「影像集」欄位中至少有一個項目包含冒號，則假設e-catalog set
   * 如果記錄「影像集」欄位中至少有一個項目包含兩個分號，則假設媒體已設定。
   * 如果記錄「影像集」欄位中至少有一個項目包含一個分號，則假設影像集。
   * 假設沒有任何項目包含冒號或分號，但至少有一個項目包含參考集或行內集（這是2D回轉集），則假設回轉集。
   * 如果沒有包含冒號或分號或參考集或行內集的條目（即以逗號分隔的影像清單），則假設未知集。

* 如果在影像AND靜態內容目錄中都找到記錄

   * 如果副檔名如下，則假設有視訊：mp3, mp4, flv, f4v, swf, xml
   * 假設影像

* 如果在靜態內容目錄中找到記錄，但在映像目錄中找不到記錄

   * 如果副檔名如下，則假設有視訊：mp3, mp4, flv, f4v, swf, xml
   * 假設靜態，否則

* 如果在影像目錄中找到記錄，但在靜態內容目錄中找不到記錄

   * 假設影像

* 如果在映像目錄中找不到記錄，而在靜態內容目錄中找不到記錄

   * 如果副檔名如下，則假設是以檔案為基礎的視訊：mp3, mp4, flv, f4v, swf, xml
   * 假設以檔案為基礎的影像

在所有情況下，產生的xml回應都符合指定的XML檔案，其中設定根節點與偵測到的類型對應。

## 內置類型檢測{#section-8f46490e467247e69ce284704def06f3}

當檢測到外部組為類型介質集時，響應將包含一組與`catalog::ImageSet`中每個介質集條目對應的介質集項目。 如果為特定媒體集條目指定了可選類型參數，則該參數將根據下表映射到輸出類型：

| 輸入類型 | 輸出類型 |
|---|---|
| `img` | `img` |
| `basic` | `img` |
| `advanced_image` | `img` |
| `img_set` | `img_set` |
| `advanced_image_set` | `img_set` |
| `advanced_swatchset` | `img_set` |
| `spin` | `spin` |
| `video` | `video` |
| `video_set` | `video_set` |
| `static` | `static` |
| `ecat` | `ecat` |

如果未指定特定媒體集條目的可選類型參數或與不支援的類型相對應，則使用與在外部設定級別應用的相同規則自動檢測媒體集條目類型。

## XML規範{#section-c1bd60948ef545759a16885bb6fcc607}

傳回的xml回應符合下列規格：

`http://crc.scene7.com/is-docs/examples/mediaset.dtd`

## LabelKey {#section-bf565de6f7294cf89620343c9071f415}

`labelkey=`修飾詞與`catalog::UserData`欄位一起使用，以產生影像和色票的標籤。 `catalog:UserData`欄位被解析為一組鍵／值對，並且該集中的標籤鍵索引用於檢索給定鍵的值。 然後，在&#x200B;*`s`*&#x200B;和&#x200B;*`i`*&#x200B;的&#x200B;*`l`*&#x200B;屬性中返回此值。

## 強制限制{#section-b9f042873bee45a5ae11b69fd42f2bca}

為了限制響應的大小並防止自引用問題，最大嵌套深度由伺服器屬性`PS::fvctx.nestingLimit`控制。 如果超過此限制，則會傳回錯誤。

為了限制大型e-catalog集的xml響應的大小，會根據伺服器屬性`PS::fvctx.brochureLimit`來抑制手冊集項的專用元資料。 所有與手冊相關的私人中繼資料都會匯出，直到手冊限制達到為止。 一旦超出限制，私有映射和用戶資料將被隱藏，並且將設定相應的標誌來指示隱藏的資料類型。

不支援巢狀媒體集。 嵌套媒體集被定義為包含介質集類型的介質集。 如果偵測到此情況，則會傳回錯誤。

## 範例 {#section-588c9d33aa05482c86cd2b1936887228}

有關`req=set`請求的XML回應範例，請參閱「HTML範例」標題下的「屬性」頁面。

`http://crc.scene7.com/is-docs/examples/properties.htm`

## 另請參閱 {#section-625ec466c948476e800dc0c52a4532d3}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) ,  [imageset=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3), catalog::ImageSet [, ](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md) [Image Catalog Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)

