---
description: 「影像伺服」提供一種機制，用於擷取階層文字回應（xml或json），該回應代表與特定記錄的目錄ImageSet相關的所有資源和中繼資料。
solution: Experience Manager
title: 媒體集要求
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71efed33-6248-4d23-ab4e-2caec3449171
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 0%

---

# 媒體集要求{#media-set-requests}

「影像伺服」提供一種機制，用於擷取階層文字回應（xml或json），該回應代表與特定記錄的catalog：：ImageSet相關聯的所有資源和中繼資料。

檢視者可以使用此機制產生回應，以告知簡報簡單影像、影片、影片集、色票集、迴轉集、頁面集(e-catalog)和媒體集。

## 要求語法 {#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

可以使用`req=set`修飾元並參考網路路徑中的目錄記錄ID，來擷取`catalog::ImageSet`的設定回應。 或者，可以使用`imageset=`修飾元直接在URL中指定影像集。 如果使用`imageset=`修飾元來指定影像集，則整個值應括在大括弧中，以便逸出影像集值並確保任何包含的修飾元不會解譯為URL查詢字串的一部分。

## 集合回應的型別 {#section-93eb0a1f70344da2a888e56372ad3896}

設定機制支援下列型別的回應：

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>簡單影像 </p></td> 
  <td class="stentry"> <p>未定義<span class="codeph">目錄：：ImageSet</span>的影像記錄。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>簡單影片 </p></td> 
  <td class="stentry"> <p>靜態內容目錄中的視訊記錄。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>色票集 </p></td> 
  <td class="stentry"> <p>一組專案，包含影像記錄的參照和作為色票使用的影像記錄的選擇性個別參照。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>階層式色票集 </p></td> 
  <td class="stentry"> <p>一組專案，包含基本色票專案或色票集記錄的參照。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>迴轉集 </p></td> 
  <td class="stentry"> <p>由影像ID的簡單清單組成的一組專案。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>二維迴轉集 </p></td> 
  <td class="stentry"> <p>由簡單影像或基本迴轉集參照組成的一組專案。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>頁面集 </p></td> 
  <td class="stentry"> <p>一組專案，包含最多三個頁面影像的清單 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>媒體集 </p></td> 
  <td class="stentry"> <p>一組專案，包含簡單影像、視訊集、色票集、階層式色票集、迴轉集、二維迴轉集、頁面集和視訊資產。 每個媒體集專案也可以包含選用的色票。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>視訊集 </p></td> 
  <td class="stentry"> <p>由簡單影片清單組成的一組專案。 </p></td> 
 </tr> 
</table>

## 外部集合型別偵測 {#section-3dd6e453528d46898e559d31458a59ba}

收到`req=set`要求時，要產生的回應型別由`catalog::AssetType`的值決定。 如果未定義`catalog::AssetType`，則回應型別由下列規則決定：

* 如果在影像目錄中找到記錄且已定義`catalog::ImageSet`

   * 如果記錄影像集欄位中至少有一個專案包含冒號，則假設電子目錄集
   * 如果記錄影像集欄位中至少有一個專案包含兩個分號，則假設媒體已設定。
   * 如果記錄影像集欄位中至少有一個專案包含一個分號，則假設影像集。
   * 如果沒有任何專案包含冒號或分號，但至少有一個專案包含參考集或內嵌集（這是2D迴轉集），請假設迴轉集。
   * 如果沒有專案包含冒號、分號、參照集合或內嵌集合（亦即以逗號分隔的影像清單），則假設為未知集合。

* 如果在影像和靜態內容目錄中都能找到記錄

   * 如果檔案副檔名為下列集，則假設視訊： mp3、mp4、flv、f4v、swf、xml
   * 否則，假設影像

* 如果在靜態內容目錄中找到記錄，但未在影像目錄中找到

   * 如果檔案副檔名為下列集，則假設視訊： mp3、mp4、flv、f4v、swf、xml
   * 假設為靜態，否則

* 如果在影像目錄中找到記錄但未在靜態內容目錄中找到

   * 假設影像

* 如果在影像目錄中找不到記錄，且在靜態內容目錄中找不到

   * 如果檔案副檔名是以下組合，則假設使用檔案式視訊： mp3、mp4、flv、f4v、swf、xml
   * 否則採用檔案型影像

在所有情況下，產生的xml回應會符合指定的XML檔案，且設定根節點會對應偵測到的型別。

## 內部集合型別偵測 {#section-8f46490e467247e69ce284704def06f3}

當偵測到外部集為型別媒體集時，回應會包含一組媒體集專案，這些專案與`catalog::ImageSet`中的每個媒體集專案相對應。 如果為特定媒體集專案指定了可選的型別引數，則會根據下表將其對應至輸出型別：

| 輸入類型 | 輸出型別 |
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

如果未指定特定媒體集專案的選擇性型別引數，或該引數對應至不支援的型別，則會使用與套用至外部集層級的規則相同的規則來自動偵測媒體集專案型別。

## XML規格 {#section-c1bd60948ef545759a16885bb6fcc607}

傳回的xml回應符合以下規格：

`http://crc.scene7.com/is-docs/examples/mediaset.dtd`

## 標籤索引鍵 {#section-bf565de6f7294cf89620343c9071f415}

`labelkey=`修飾元與`catalog::UserData`欄位搭配使用，以產生影像和色票的標籤。 `catalog:UserData`欄位會剖析為一組索引鍵/值配對，而此組中的labelkey索引會擷取指定索引鍵的值。 然後會在&#x200B;*`s`*&#x200B;和&#x200B;*`i`*&#x200B;的&#x200B;*`l`*&#x200B;屬性中傳回此值。

## 強制的限制 {#section-b9f042873bee45a5ae11b69fd42f2bca}

為了限制回應的大小並防止自我參照問題，最大巢狀深度是由伺服器屬性`PS::fvctx.nestingLimit`所控制。 如果超過此限制，則會傳回錯誤。

為了限制大型e-catalog集的xml回應大小，會根據伺服器屬性`PS::fvctx.brochureLimit`抑制手冊集專案的私人中繼資料。 會匯出與手冊相關的所有私人中繼資料，直到達到手冊限製為止。 超過限制後，會隱藏私人地圖和使用者資料，並設定對應的旗標，以指出隱藏的資料型別。

不支援巢狀媒體集。 巢狀媒體集定義為包含型別媒體集的媒體集專案的媒體集。 如果偵測到這種情況，則會傳回錯誤。

## 範例 {#section-588c9d33aa05482c86cd2b1936887228}

如需`req=set`要求的範例XML回應，請參閱HTML範例標頭底下的「屬性」頁面。

`http://crc.scene7.com/is-docs/examples/properties.htm`

## 另請參閱 {#section-625ec466c948476e800dc0c52a4532d3}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) ， [影像集=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3)， [目錄：：ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md)， [影像目錄參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
