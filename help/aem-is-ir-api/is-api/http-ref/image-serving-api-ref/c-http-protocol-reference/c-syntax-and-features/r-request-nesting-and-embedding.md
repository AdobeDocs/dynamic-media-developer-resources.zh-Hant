---
description: 「影像提供」支援無限巢狀的影像提供請求、內嵌影像轉譯請求，以及內嵌從外部伺服器擷取的影像。 只有圖層影像和圖層遮罩支援這些機制。
solution: Experience Manager
title: 請求巢狀和內嵌
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b9c9d241-5a3d-4637-a90a-d8cdf29cc968
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 0%

---

# 請求巢狀和內嵌{#request-nesting-and-embedding}

「影像提供」支援無限巢狀的影像提供請求、內嵌影像轉譯請求，以及內嵌從外部伺服器擷取的影像。 只有圖層影像和圖層遮罩支援這些機制。

>[!NOTE]
>
>某些電子郵件用戶端和代理伺服器可能會將用於巢狀和內嵌語法的大括弧編碼。 對於此問題，應使用括弧而非大括弧。

## 巢狀影像伺服請求 {#section-6954202119e0466f8ff27c79f4f039c8}

使用下列語法，在`src=`（或`mask=`）命令中指定整個影像伺服請求，即可將其用作圖層源：

`…&src=is( nestedRequest)&…`

`is`代號區分大小寫。

巢狀請求不得包含伺服器根路徑（通常為` http:// *[!DNL server]*/is/image/'`）。

>[!NOTE]
>
>巢狀請求中的巢狀請求分隔字元(`'(',')'`)和命令分隔字元(`'?'`、`'&'`、`'='`)不得進行HTTP編碼。 有效地，巢狀請求的編碼必須與外部（巢狀）請求相同。

預處理規則會套用至巢狀請求。

在巢狀請求中指定時（在請求URL中、在`catalog::Modifier`或`catalog::PostModifier`中），會忽略下列命令：

* `fmt=`
* `qlt=`
* `iccEmbed=`
* `printRes=`
* `quantize=`
* `req=`
* `bgc=`

如果巢狀請求的結果影像包含遮罩(Alpha)資料，則會將其作為圖層遮罩傳遞至內嵌層。

套用至巢狀請求的影像目錄的`attribute::MaxPix`和`attribute::DefaultPix`也會遭到忽略。

可選擇包含`cache=on`來快取巢狀IS請求的影像結果。 預設會停用中繼資料的快取。 只有當中間映像預期在合理的時間段內在不同請求中重複使用時，才應啟用快取。 標準伺服器端快取管理適用。 資料以無損格式快取。

## 內嵌影像轉譯請求 {#section-69c5548db930412b9b90d9b2951a6969}

在伺服器上啟用Dynamic Media影像呈現時，可在src=（或mask=）命令中指定呈現請求，將其用作圖層源。 使用下列語法：

` …&src=ir( *[!DNL renderRequest]*)&…`

`ir`代號區分大小寫。

*[!DNL renderRequest]* 是通常的影像呈現請求，但HTTP根路徑除外 ` http:// *[!DNL server]*/ir/render/`。

>[!NOTE]
>
>巢狀請求中的巢狀請求分隔字元(`'(',')'`)和命令分隔字元(`'?'`、`'&'`、`'='`)不得進行HTTP編碼。 有效地，內嵌請求的編碼必須與外部（內嵌）請求的編碼相同。

在巢狀請求中指定時，會忽略下列影像呈現命令：

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`

套用至巢狀轉譯請求的材料目錄的`attribute::MaxPix`和`attribute::DefaultPix`也會遭到忽略。

可選擇性地通過包括`cache=on`來快取嵌套IR請求的影像結果。 預設會停用中繼資料的快取。 只有當中間映像預期在合理的時間段內在不同請求中重複使用時，才應啟用快取。 標準伺服器端快取管理適用。 資料以無損格式快取。

## 內嵌FXG轉譯請求 {#section-c817e4b4f7da414ea5a51252ca7e120a}

當安裝FXG圖形呈現器（也稱為[!DNL AGMServer]）並啟用影像伺服時，可在`src=`（或`mask=`）命令中指定FXG請求作為層源使用。 使用下列語法：

`…&src=fxg( renderRequest)&…`

`fxg`代號區分大小寫。

>[!NOTE]
>
>FXG圖形呈現僅在Dynamic Media托管環境中提供，可能需要額外授權。 如需詳細資訊，請聯絡Dynamic Media技術支援。

*[!DNL renderRequest]* 是通常的FXG轉譯請求，排除HTTP根路 ` http:// *[!DNL server]*/agm/render/`徑。

>[!NOTE]
>
>巢狀請求中的分隔字元(`'(',')'`)和命令分隔字元(`'?'`、`'&'`、`'='`)不得進行HTTP編碼。 有效地，內嵌請求的編碼必須與外部（內嵌）請求的編碼相同。

在巢狀請求中指定時，會忽略下列FXG命令：

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `cache=`

## 外國影像源 {#section-84e83ecfcd1a43748cdfc7a6f8c04cb8}

「影像伺服」支援對外部HTTP伺服器上源影像的訪問。

>[!NOTE]
>
>遠端URL僅支援HTTP通訊協定。

若要為`src=`或`mask=`命令指定外來URL，請以括弧分隔外來URL或URL片段：

`…&src=( foreignUrl)&…`

重要：巢狀請求中的分隔字元(`'(',')'`)和命令分隔字元(`'?'`、`'&'`、`'='`)不得進行HTTP編碼。 有效地，內嵌請求的編碼必須與外部（內嵌）請求的編碼相同。

允許完整絕對URL（若已設定`attribute::AllowDirectUrls`），且允許相對於`attribute::RootUrl`的URL。 如果內嵌絕對URL和屬性，則會發生錯誤：`AllowDirectUrls`為0，或者如果指定了相對URL且`attribute::RootUrl`為空。

雖然無法直接在請求URL的路徑元件中指定外來URL，但您可以設定預處理規則，以允許將相對路徑轉換為絕對URL（請參閱以下範例）。

伺服器會根據HTTP回應所包含的快取標題，快取外部影像。 如果`ETag`或上次修改的HTTP回應標頭均不存在，則不會快取回應。 這可能會導致對相同外來影像重複存取時效能不佳，因為影像伺服每次存取時都需要重新擷取和重新驗證影像。

此機制支援與Image Convert(IC)實用程式支援的影像檔案格式相同，但源影像的每元件16位元除外。

>[!NOTE]
>
>當首次使用外來映像時，映像服務將自動運行驗證實用程式，以確保映像有效且在傳輸期間未損壞。 這可能會導致首次存取稍微延遲。 為獲得最佳效能，建議限制此類影像的大小和/或使用壓縮良好的影像檔案格式。

## 限制 {#section-fb68e3f0d40947feb94d7bf183b64929}

巢狀/內嵌請求產生的影像大小通常會自動最佳化。 如果啟用了嵌套請求影像的快取，則可以通過指定嵌套影像的確切大小來實現增量效能增益，因此在重複使用快取項時不需要進一步縮放。

「重要影像伺服」不支援對巢狀或內嵌的請求進行雙重編碼。 巢狀和內嵌的要求必須像簡單要求一樣以HTTP編碼。

## 範例 {#section-d800cfc31abe46d2a964f8e7929231f1}

**具有快取的分層模板：**

使用嵌套將快取添加到分層模板。 有限數量的背景影像重疊有高度可變的文字。 初始範本字串可能如下所示：

`layer=0&src=$img$&size=300,300&layer=1&text=$txt$`

只要稍作修改，我們就可以預先縮放第0層映像並永久快取它，從而減少伺服器負載：

`layer=0&src=is(?src=$img$&size=300,300&cache=on)&layer=1&text=$txt$`

**Dynamic Media影像轉譯的內嵌請求**

使用儲存在[!DNL myCatalog/myTemplate]中的模板；使用Dynamic Media影像呈現為範本的第2層產生影像：

`http://server/is/image/myCatalog/myTemplate?layer=2&src=ir(myRenderCatalog/myRenderObject?id=myIdValue&sel=group&src=is(myCatalog/myTexture1?res=30)&res=30)&wid=300`

記下巢狀大括弧。 影像呈現請求會內嵌回影像伺服的呼叫，以擷取可重複的紋理。

## 另請參閱 {#section-109a0a9a3b144158958351139c8b8e69}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)，要求預 [先處理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-preprocessing.md#reference-c27976436bf04194bfbe9adf40ea98e3)，影像呈現參考， [範本](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e),  [影像伺服公用程式](../../../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)
