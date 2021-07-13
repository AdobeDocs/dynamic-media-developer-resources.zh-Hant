---
description: 「影像伺服」提供一種擷取階層式文字回應（xml或json）的機制，該回應代表與特定記錄的目錄ImageSet相關聯的所有資源和中繼資料。
solution: Experience Manager
title: 媒體集請求
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71efed33-6248-4d23-ab4e-2caec3449171
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '967'
ht-degree: 0%

---

# 媒體集請求{#media-set-requests}

「影像伺服」提供擷取階層式文字回應（xml或json）的機制，該回應代表與特定記錄的catalog::ImageSet相關聯的所有資源和中繼資料。

檢視器可使用此機制產生回應，以通知簡單影像、視訊、視訊集、色票集、回轉集、頁面集(e-catalog)和媒體集的呈現方式。

## 要求語法 {#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

可使用`req=set`修飾符並參考淨路徑中的目錄記錄ID來檢索`catalog::ImageSet`的設定響應。 或者，您也可以使用`imageset=`修飾元，直接在URL中指定影像集。 如果使用`imageset=`修飾詞來指定影像集，則應將整個值括在大括弧中，以逸出影像集值，並確保任何包含的修飾詞不被解譯為URL查詢字串的一部分。

## 設定回應的類型 {#section-93eb0a1f70344da2a888e56372ad3896}

設定機制支援下列類型的回應：

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>簡單影像 </p></td> 
  <td class="stentry"> <p>未定義<span class="codeph">目錄：:ImageSet</span>的影像記錄。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>簡單影片 </p></td> 
  <td class="stentry"> <p>靜態內容目錄中的視訊記錄。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>色票集 </p></td> 
  <td class="stentry"> <p>一組項，包括對影像記錄的引用和對用作色票的影像記錄的可選單獨引用。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>分層色票集 </p></td> 
  <td class="stentry"> <p>由基本色板項或對色板集記錄的引用組成的一組項。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>回轉集 </p></td> 
  <td class="stentry"> <p>一組項目，包含簡單的影像ID清單。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>二維自旋集 </p></td> 
  <td class="stentry"> <p>由簡單影像或基本回轉集的參照組成的項目集。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>頁面集 </p></td> 
  <td class="stentry"> <p>一組項目，包含最多三個頁面影像的清單 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>媒體集 </p></td> 
  <td class="stentry"> <p>由簡單影像、視訊集、色票集、階層式色票集、回轉集、二維回轉集、頁面集和視訊資產組成的一組項目。 每個媒體集項目也可包含選用色票。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>視訊集 </p></td> 
  <td class="stentry"> <p>由簡單影片清單組成的項目集。 </p></td> 
 </tr> 
</table>

## 外置式檢測 {#section-3dd6e453528d46898e559d31458a59ba}

收到`req=set`請求時，要生成的響應類型由`catalog::AssetType`的值確定。 如果未定義`catalog::AssetType`，則響應類型由以下規則確定：

* 如果在映像目錄中找到記錄，則定義`catalog::ImageSet`

   * 如果記錄「影像集」欄位中至少有一個條目包含冒號，則假定設定電子目錄
   * 如果「記錄影像集」欄位中至少有一個條目包含兩個分號，則假設介質已設定。
   * 如果「記錄影像集」欄位中至少有一個條目包含一個分號，則假設已設定影像。
   * 如果沒有任何項目包含冒號或分號，但至少有一個項目包含引用集或行內集（這是2D回轉集），則假設為回轉集。
   * 如果沒有任何條目包含冒號、分號、引用集或行內集（即以逗號分隔的影像清單），則假設未知集。

* 如果在影像和靜態內容目錄中都找到記錄

   * 如果檔案副檔名如下，則假設為video :mp3, mp4, flv, f4v, swf, xml
   * 假設影像

* 如果在靜態內容目錄中找到記錄，但在影像目錄中找不到記錄

   * 如果檔案副檔名如下，則假設為video :mp3, mp4, flv, f4v, swf, xml
   * 假設為靜態

* 如果在影像目錄中找到記錄，但在靜態內容目錄中找不到

   * 假設影像

* 如果在映像目錄中找不到記錄，且在靜態內容目錄中找不到記錄

   * 如果副檔名如下，則假設為檔案式視訊：mp3, mp4, flv, f4v, swf, xml
   * 假設基於檔案的影像

在所有情況下，結果的xml響應都將符合指定的XML文檔，並設定與檢測到的類型對應的根節點。

## 內置式檢測 {#section-8f46490e467247e69ce284704def06f3}

當檢測到外部集為類型媒體集時，響應將包含與`catalog::ImageSet`中的每個媒體集條目對應的一組媒體集項。 如果為特定媒體集條目指定了可選類型參數，則將根據下表將其映射到輸出類型：

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

如果未指定特定媒體集條目的可選類型參數或與不支援的類型相對應，則使用與在外部集級別應用的相同規則自動檢測媒體集項目類型。

## XML規範 {#section-c1bd60948ef545759a16885bb6fcc607}

返回的xml響應符合以下規範：

`http://crc.scene7.com/is-docs/examples/mediaset.dtd`

## LabelKey {#section-bf565de6f7294cf89620343c9071f415}

`labelkey=`修飾符與`catalog::UserData`欄位一起使用，以生成影像和色票的標籤。 將`catalog:UserData`欄位解析為一組鍵/值對，並將labelkey索引到此集以檢索給定鍵的值。 然後，在&#x200B;*`s`*&#x200B;和&#x200B;*`i`*&#x200B;的&#x200B;*`l`*&#x200B;屬性中返回此值。

## 強制限制 {#section-b9f042873bee45a5ae11b69fd42f2bca}

為了限制回應的大小並防止自我參考問題，最大嵌套深度由伺服器屬性`PS::fvctx.nestingLimit`控制。 如果超過此限制，則會傳回錯誤。

為了限制大型電子目錄集的xml響應的大小，根據伺服器屬性`PS::fvctx.brochureLimit`來抑制手冊集項的私有元資料。 與手冊相關聯的所有私人中繼資料都會匯出，直到手冊限制達到為止。 一旦超出限制，將隱藏私有地圖和用戶資料，並設定相應的標誌，以指示隱藏的資料類型。

不支援巢狀媒體集。 巢狀媒體集定義為包含媒體集類型媒體集項目的媒體集。 如果偵測到此條件，則會傳回錯誤。

## 範例 {#section-588c9d33aa05482c86cd2b1936887228}

有關`req=set`請求的XML回應範例，請參閱HTML範例標題下的屬性頁面。

`http://crc.scene7.com/is-docs/examples/properties.htm`

## 另請參閱 {#section-625ec466c948476e800dc0c52a4532d3}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) ,  [imageset=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3),  [catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md),  [Image Catalog Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
