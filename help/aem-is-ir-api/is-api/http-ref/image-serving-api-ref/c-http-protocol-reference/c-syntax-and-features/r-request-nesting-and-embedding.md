---
description: 「影像伺服」支援無限制的「影像伺服」請求巢狀、內嵌「影像演算」請求，以及內嵌從外部伺服器擷取的影像。 只有圖層影像和圖層遮色片才支援這些機制。
seo-description: 「影像伺服」支援無限制的「影像伺服」請求巢狀、內嵌「影像演算」請求，以及內嵌從外部伺服器擷取的影像。 只有圖層影像和圖層遮色片才支援這些機制。
seo-title: 請求巢狀內嵌
solution: Experience Manager
title: 請求巢狀內嵌
topic: Scene7 Image Serving - Image Rendering API
uuid: 59031329-e65f-4631-bc7d-83f2540cc836
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 請求巢狀內嵌{#request-nesting-and-embedding}

「影像伺服」支援無限制的「影像伺服」請求巢狀、內嵌「影像演算」請求，以及內嵌從外部伺服器擷取的影像。 只有圖層影像和圖層遮色片才支援這些機制。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>某些電子郵件用戶端和代理伺服器可能會編碼用於巢狀和內嵌語法的大括弧。 對於此問題，應用程式應使用括弧而非大括弧。

## 巢狀影像伺服請求 {#section-6954202119e0466f8ff27c79f4f039c8}

使用下列語法，在（或）命令中指定整個影像伺服請求， `src=` 即可將其用 `mask=`作圖層來源：

`…&src=is( nestedRequest)&…`

代 `is` 號區分大小寫。

巢狀請求不得包含伺服器根路徑(通常 ` http:// *[!DNL server]*/is/image/'`)。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>巢狀請求中的巢狀請求分隔字 `'(',')'`元()和命令分隔字元( `'?'`, `'&'`, `'='`)不得使用HTTP編碼。 有效地，巢狀請求的編碼必須與外部（巢狀）請求相同。

預處理規則會套用至巢狀請求。

在巢狀請求中指定（在請求URL中或在或中）時，會忽略 `catalog::Modifier` 下列命 `catalog::PostModifier`令：

* `fmt=`
* `qlt=`
* `iccEmbed=`
* `printRes=`
* `quantize=`
* `req=`
* `bgc=`

如果巢狀請求的結果影像包括掩碼(alpha)資料，則將其作為層掩碼傳遞到嵌入層。

也會忽略套 `attribute::MaxPix`用至 `attribute::DefaultPix` 巢狀請求的影像目錄和影像目錄。

巢狀IS請求的影像結果可選擇性地加入以快取 `cache=on`。 預設情況下，會禁用中間資料的快取。 只有當中間影像預期在合理時段內於不同請求中重複使用時，才應啟用快取。 套用標準伺服器端快取管理。 資料以無損格式快取。

## 內嵌影像演算請求 {#section-69c5548db930412b9b90d9b2951a6969}

在伺服器上啟用Scene7影像演算時，演算請求可在src=（或mask=）命令中指定，以做為圖層來源。 使用下列語法：

` …&src=ir( *[!DNL renderRequest]*)&…`

代 `ir` 號區分大小寫。

*[!DNL renderRequest]* 是通常的「影像演算」請求，排除HTTP根路徑 ` http:// *[!DNL server]*/ir/render/`。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>巢狀請求中的巢狀請求分隔字 `'(',')'`元()和命令分隔字元( `'?'`, `'&'`, `'='`)不得使用HTTP編碼。 有效地，內嵌請求的編碼必須與外部（內嵌）請求相同。

在巢狀請求中指定下列影像演算命令時，會忽略：

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`

也會忽略套 `attribute::MaxPix` 用至 `attribute::DefaultPix` 巢狀演算請求的材質目錄。

可選擇性地通過包括來快取嵌套IR請求的影像結果 `cache=on`。 預設情況下，會禁用中間資料的快取。 只有當中間影像預期在合理時段內於不同請求中重複使用時，才應啟用快取。 套用標準伺服器端快取管理。 資料以無損格式快取。

## 內嵌的FXG轉譯請求 {#section-c817e4b4f7da414ea5a51252ca7e120a}

當FXG圖形轉換器(亦即 [!DNL AGMServer])安裝並啟用「影像伺服」時，FXG請求可在(或 `src=``mask=`)指令中指定，以做為圖層來源。 使用下列語法：

`…&src=fxg( renderRequest)&…`

代 `fxg` 號區分大小寫。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>FXG圖形演算僅適用於Scene7代管環境，可能需要額外授權。 如需詳細資訊，請連絡Scene7支援。

*[!DNL renderRequest]* 是通常的FXG演算請求，排除HTTP根路徑 ` http:// *[!DNL server]*/agm/render/`。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>巢狀請求中的分隔字 `'(',')'`元()和命令分隔字元( `'?'`、 `'&'`、 `'='`)不得使用HTTP編碼。 有效地，內嵌請求的編碼必須與外部（內嵌）請求相同。

在巢狀請求中指定下列FXG命令時，將忽略：

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `cache=`

## 外來影像來源 {#section-84e83ecfcd1a43748cdfc7a6f8c04cb8}

「影像伺服」支援存取外來HTTP伺服器上的來源影像。

>[!NOTE]
>
>遠端URL僅支援HTTP通訊協定。

要為或命令指定外 `src=` 來URL, `mask=` 請用括弧分隔外來URL或URL片段：

`…&src=( foreignUrl)&…`

重要：巢狀請求中 `'(',')'`的分隔字元()和命令分隔字元( `'?'`, `'&'`, `'='`)不得使用HTTP編碼。 有效地，內嵌請求的編碼必須與外部（內嵌）請求相同。

完整絕對URL(如 `attribute::AllowDirectUrls` 果已設定)，且允許相對 `attribute::RootUrl` 於URL。 如果嵌入了絕對URL且屬性： `AllowDirectUrls` 為0，或指定相對URL且空 `attribute::RootUrl` 白。

雖然無法直接在請求URL的路徑元件中指定外來URL，但是可以設定預處理規則，以允許將相對路徑轉換為絕對URL（請參閱以下範例）。

伺服器會根據HTTP回應所包含的快取標題，快取外來影像。 如果既不存 `ETag` 在「上次修改的HTTP」回應標頭，則不會快取回應。 這可能會導致相同外來影像重複存取時效能不佳，因為「影像伺服」需要在每次存取時重新擷取並重新驗證影像。

此機制支援與影像轉換(IC)實用程式支援的影像檔案格式相同，但每個元件16位的源影像除外。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>當首次使用外來映像時，映像服務將自動運行驗證實用程式，以確保映像有效且在傳輸過程中未損壞。 這可能會導致首次訪問的輕微延遲。 為獲得最佳效能，建議限制此類影像的大小和／或使用壓縮良好的影像檔案格式。

## Restrictions {#section-fb68e3f0d40947feb94d7bf183b64929}

巢狀／內嵌請求所產生的影像大小通常會自動最佳化。 如果啟用了嵌套請求影像的快取，則可以通過指定嵌套影像的確切大小來實現增量效能提升，因此當重新使用快取條目時不需要進一步縮放。

重要：影像伺服不支援對巢狀或內嵌請求進行雙重編碼。 巢狀和內嵌的請求必須像簡單請求一樣HTTP編碼。

## 範例 {#section-d800cfc31abe46d2a964f8e7929231f1}

**使用快取分層範本：**

使用巢狀功能將快取新增至分層範本。 有限數量的背景影像會覆蓋高度可變的文字。 初始範本字串可能如下所示：

`layer=0&src=$img$&size=300,300&layer=1&text=$txt$`

只要稍加修改，我們就可以預先縮放第0層影像並持續快取它，從而降低伺服器負載：

`layer=0&src=is(?src=$img$&size=300,300&cache=on)&layer=1&text=$txt$`

**內嵌Scene7影像演算要求**

使用儲存在中的模板 [!DNL myCatalog/myTemplate];使用Scene7影像演算為範本的layer2產生影像：

`http://server/is/image/myCatalog/myTemplate?layer=2&src=ir(myRenderCatalog/myRenderObject?id=myIdValue&sel=group&src=is(myCatalog/myTexture1?res=30)&res=30)&wid=300`

請注意巢狀大括弧。 「影像演算」要求會內嵌回呼「影像服務」，以擷取可重複的紋理。

## 另請參閱 {#section-109a0a9a3b144158958351139c8b8e69}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , mask= [，請求預處理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)，影像渲染參考，模板 [，模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-preprocessing.md#reference-c27976436bf04194bfbe9adf40ea98e3)，影像服 [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)[務實用程式](../../../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)
