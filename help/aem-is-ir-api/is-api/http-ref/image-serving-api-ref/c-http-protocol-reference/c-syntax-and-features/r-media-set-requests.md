---
description: Image Serving提供了一種獲取層次文本響應（xml或json）的機制，該文本響應表示與特定記錄的目錄ImageSet關聯的所有資源和元資料。
solution: Experience Manager
title: 媒體集請求
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71efed33-6248-4d23-ab4e-2caec3449171
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '957'
ht-degree: 0%

---

# 媒體集請求{#media-set-requests}

Image Serving提供了一種獲取層次文本響應（xml或json）的機制，該響應表示與特定記錄的目錄：:ImageSet關聯的所有資源和元資料。

觀看者可以使用此機制來生成響應，以通知簡單影像、視頻、視頻集、色板集、旋轉集、頁集（e目錄）和媒體集的呈現。

## 請求語法 {#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

為 `catalog::ImageSet` 可使用 `req=set` 修改量並引用淨路徑中的目錄記錄id。 或者，可以使用 `imageset=` 修改量。 如果 `imageset=` 修飾符用於指定影像集，應將整個值括在大括弧中，以轉義影像集值，並確保所有包含的修飾符不被解釋為URL查詢字串的一部分。

## 集響應的類型 {#section-93eb0a1f70344da2a888e56372ad3896}

設定機制支援以下類型的響應：

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>簡單影像 </p></td> 
  <td class="stentry"> <p>沒有 <span class="codeph"> 目錄：:ImageSet</span> 定義。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>簡單的視頻 </p></td> 
  <td class="stentry"> <p>靜態內容目錄中的視頻記錄。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>樣本集 </p></td> 
  <td class="stentry"> <p>一組項，包括對影像記錄的引用和對用作樣本的影像記錄的可選單獨引用。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>分層樣本集 </p></td> 
  <td class="stentry"> <p>由基本色板項或對色板集記錄的引用組成的一組項。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>自旋集 </p></td> 
  <td class="stentry"> <p>由簡單影像ID清單組成的一組項。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>二維自旋集 </p></td> 
  <td class="stentry"> <p>一組由簡單影像或對基本自旋集的引用組成的項目。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>頁集 </p></td> 
  <td class="stentry"> <p>由最多三張頁面影像的清單組成的一組項目 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>媒體集 </p></td> 
  <td class="stentry"> <p>一組由簡單影像、視頻集、色板集、分層色板集、旋轉集、二維旋轉集、頁集和視頻資產組成的項目。 每個媒體集項目也可包含可選色板。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>視頻集 </p></td> 
  <td class="stentry"> <p>一組由簡單視頻清單組成的項目。 </p></td> 
 </tr> 
</table>

## 外置型檢測 {#section-3dd6e453528d46898e559d31458a59ba}

當 `req=set` 接收請求，由生成的響應的值確定 `catalog::AssetType`。 如果 `catalog::AssetType` 未定義，則響應類型由以下規則確定：

* 如果在映像目錄AND中找到記錄 `catalog::ImageSet` 定義

   * 如果記錄「影像集」欄位中至少有一個條目包含冒號，則假定電子目錄集
   * 如果「記錄影像集」欄位中至少有一個條目包含兩個分號，則假設媒體集。
   * 如果記錄「影像集」欄位中至少有一個條目包含一個分號，則假定影像集。
   * 如果沒有條目包含冒號或分號，但至少有一個條目包含引用集或行內集（這是2D旋轉集），則假定為旋轉集。
   * 如果沒有條目包含冒號、分號、引用集或行內集（即以逗號分隔的影像清單），則假設未知集。

* 如果在映像AND靜態內容目錄中都找到記錄

   * 如果檔案副檔名在以下設定中，則假定視頻：mp3、mp4、flv、f4v、swf、xml
   * 假設影像

* 如果在靜態內容目錄中找到記錄，但在映像目錄中未找到記錄

   * 如果檔案副檔名在以下設定中，則假定視頻：mp3、mp4、flv、f4v、swf、xml
   * 假設靜態

* 如果在映像目錄中找到記錄，但在靜態內容目錄中找不到

   * 假設影像

* 如果在影像目錄中未找到記錄，在靜態內容目錄中找不到記錄

   * 如果檔案副檔名在以下集中，則假定基於檔案的視頻：mp3、mp4、flv、f4v、swf、xml
   * 假定基於檔案的影像

在所有情況下，生成的xml響應都將符合指定的XML文檔，其設定的根節點對應於檢測到的類型。

## 內置型檢測 {#section-8f46490e467247e69ce284704def06f3}

當檢測到外部集為類型媒體集時，響應將包含一組與中的每個媒體集條目對應的媒體集條目 `catalog::ImageSet`。 如果為特定媒體集條目指定了可選類型參數，則根據下表將其映射到輸出類型：

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

如果未指定特定媒體集條目的可選類型參數或該參數對應於不受支援的類型，則使用與在外部設定級別應用的相同規則自動檢測媒體集項目類型。

## XML規範 {#section-c1bd60948ef545759a16885bb6fcc607}

返回的xml響應符合以下規範：

`http://crc.scene7.com/is-docs/examples/mediaset.dtd`

## 標籤密鑰 {#section-bf565de6f7294cf89620343c9071f415}

的 `labelkey=` 修飾符與 `catalog::UserData`欄位，以生成影像和色板的標籤。 的 `catalog:UserData` 欄位被解析為一組鍵/值對，並且此集中的labelkey索引將檢索給定鍵的值。 然後，在 *`l`* 屬性 *`s`* 和 *`i`*。

## 強制限制 {#section-b9f042873bee45a5ae11b69fd42f2bca}

為了限制響應的大小並防止自引用問題，最大嵌套深度由伺服器屬性控制 `PS::fvctx.nestingLimit`。 如果超過此限制，則返回錯誤。

為了限制大型電子目錄集的xml響應的大小，根據伺服器屬性對小冊子集項抑制專用元資料 `PS::fvctx.brochureLimit`。 與手冊關聯的所有私有元資料都會導出，直到手冊限制達到為止。 在超出該限制後，禁止私有映射和用戶資料，並設定相應標誌以指示禁止哪種類型的資料。

不支援嵌套媒體集。 嵌套媒體集定義為包含媒體集類型的媒體集項的媒體集。 如果檢測到此情況，則返回錯誤。

## 範例 {#section-588c9d33aa05482c86cd2b1936887228}

對於的XML響應示例 `req=set` 請求，請參閱「HTML示例」標題下的「屬性」頁。

`http://crc.scene7.com/is-docs/examples/properties.htm`

## 另請參閱 {#section-625ec466c948476e800dc0c52a4532d3}

[請求=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) 。 [映像集=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3)。 [目錄：:ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md)。 [影像目錄引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
