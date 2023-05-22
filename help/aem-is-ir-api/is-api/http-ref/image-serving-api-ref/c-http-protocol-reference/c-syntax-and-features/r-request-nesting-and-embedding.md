---
description: 影像服務支援影像服務請求的無限嵌套、影像呈現請求的嵌入以及從外部伺服器檢索的影像的嵌入。 只有圖層影像和圖層蒙版支援這些機制。
solution: Experience Manager
title: 請求嵌套和嵌入
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b9c9d241-5a3d-4637-a90a-d8cdf29cc968
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '1045'
ht-degree: 0%

---

# 請求嵌套和嵌入{#request-nesting-and-embedding}

影像服務支援影像服務請求的無限嵌套、影像呈現請求的嵌入以及從外部伺服器檢索的影像的嵌入。 只有圖層影像和圖層蒙版支援這些機制。

>[!NOTE]
>
>某些電子郵件客戶端和代理伺服器可以對用於嵌套和嵌入語法的花括弧進行編碼。 對於此問題的應用程式，應使用圓括弧而不是大括弧。

## 嵌套的影像服務請求 {#section-6954202119e0466f8ff27c79f4f039c8}

通過在 `src=` 或 `mask=`)命令，使用以下語法：

`…&src=is( nestedRequest)&…`

的 `is` 令牌區分大小寫。

嵌套請求不得包括伺服器根路徑(通常 ` http:// *[!DNL server]*/is/image/'`)。

>[!NOTE]
>
>嵌套請求分隔符字元( `'(',')'`)和命令分隔符( `'?'`。 `'&'`。 `'='`)中的嵌套請求不能是HTTP編碼。 有效地，嵌套請求的編碼必須與外部（嵌套）請求相同。

預處理規則應用於嵌套請求。

當在嵌套請求中指定(在請求URL中或在 `catalog::Modifier` 或 `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `iccEmbed=`
* `printRes=`
* `quantize=`
* `req=`
* `bgc=`

如果嵌套請求的結果影像包括掩碼(α)資料，則將其作為層掩碼傳遞給嵌入層。

也忽略 `attribute::MaxPix`和 `attribute::DefaultPix` 映像目錄中的「已嵌套」請求。

通過包括嵌套IS請求的影像結果可以選擇性地被快取 `cache=on`。 預設情況下，中間資料的快取被禁用。 僅當中間映像預期在合理的時間段內以不同請求重新使用時，才應啟用快取。 應用標準伺服器端快取管理。 資料以無損格式快取。

## 嵌入式影像呈現請求 {#section-69c5548db930412b9b90d9b2951a6969}

在伺服器上啟用「Dynamic Media影像呈現」後，可以在src=（或mask=）命令中指定呈現請求作為層源。 使用以下語法：

` …&src=ir( *[!DNL renderRequest]*)&…`

的 `ir` 令牌區分大小寫。

*[!DNL renderRequest]* 是通常的影像呈現請求，不包括HTTP根路徑 ` http:// *[!DNL server]*/ir/render/`。

>[!NOTE]
>
>嵌套請求分隔符字元( `'(',')'`)和命令分隔符( `'?'`。 `'&'`。 `'='`)中的嵌套請求不能是HTTP編碼。 有效地，嵌入請求的編碼必須與外部（嵌入）請求相同。

在嵌套請求中指定以下「影像呈現」命令時將忽略：

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`

也忽略 `attribute::MaxPix` 和 `attribute::DefaultPix` 應用於嵌套渲染請求的材料目錄。

通過包括嵌套IR請求的影像結果可以選擇性地被快取 `cache=on`。 預設情況下，中間資料的快取被禁用。 僅當中間映像預期在合理的時間段內以不同請求重新使用時，才應啟用快取。 應用標準伺服器端快取管理。 資料以無損格式快取。

## 嵌入式FXG呈現請求 {#section-c817e4b4f7da414ea5a51252ca7e120a}

FXG圖形呈現器時(又稱 [!DNL AGMServer])已安裝並啟用， FXG請求可通過在中指定來用作層源 `src=` 或 `mask=`)。 使用以下語法：

`…&src=fxg( renderRequest)&…`

的 `fxg` 令牌區分大小寫。

>[!NOTE]
>
>FXG圖形渲染僅在Dynamic Media托管環境中提供，可能需要額外許可。 請聯繫Dynamic Media技術支援以瞭解更多資訊。

*[!DNL renderRequest]* 是通常的FXG呈現請求，不包括HTTP根路徑 ` http:// *[!DNL server]*/agm/render/`。

>[!NOTE]
>
>分隔符字元( `'(',')'`)和命令分隔符( `'?'`。 `'&'`。 `'='`)中的嵌套請求不能是HTTP編碼。 有效地，嵌入請求的編碼必須與外部（嵌入）請求相同。

在嵌套請求中指定時，將忽略以下FXG命令：

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `cache=`

## 外來影像源 {#section-84e83ecfcd1a43748cdfc7a6f8c04cb8}

映像服務支援訪問外部HTTP伺服器上的源映像。

>[!NOTE]
>
>遠程URL僅支援HTTP協定。

指定外來URL `src=` 或 `mask=` 命令，用括弧分隔外部URL或URL片段：

`…&src=( foreignUrl)&…`

重要資訊分隔符( `'(',')'`)和命令分隔符( `'?'`。 `'&'`。 `'='`)中的嵌套請求不能是HTTP編碼。 有效地，嵌入請求的編碼必須與外部（嵌入）請求相同。

完全絕對URL(如果 `attribute::AllowDirectUrls` 設定)，以及與 `attribute::RootUrl` 的子菜單。 如果嵌入了絕對URL且屬性： `AllowDirectUrls` 為0，或者指定了相對URL並 `attribute::RootUrl` 為空。

雖然無法在請求URL的路徑元件中直接指定外來URL，但可以設定預處理規則以允許將相對路徑轉換為絕對URL（請參見下面的示例）。

伺服器根據HTTP響應所包括的快取頭對外部影像進行快取。 如果 `ETag` 也不存在上次修改的HTTP響應標頭，響應不會快取。 這可能導致對同一外部映像的重複訪問效能較差，因為映像服務需要在每次訪問時重新獲取和重新驗證映像。

此機制支援影像轉換(IC)實用程式支援的相同影像檔案格式，但每個元件16位的源影像除外。

>[!NOTE]
>
>映像服務將在首次使用外部映像時自動運行驗證實用程式，以確保映像有效且在傳輸過程中未損壞。 這可能會導致首次訪問時出現輕微延遲。 為獲得最佳效能，建議限制此類影像的大小和/或使用壓縮良好的影像檔案格式。

## 限制 {#section-fb68e3f0d40947feb94d7bf183b64929}

通常自動優化由嵌套/嵌入請求生成的影像的大小。 如果啟用嵌套請求影像的快取，可以通過指定嵌套影像的確切大小來實現增量效能增益，因此當重用快取條目時不需要進一步縮放。

重要資訊：Image Service不支援對嵌套或嵌入式請求進行雙重編碼。 嵌套和嵌入式請求必須像簡單請求一樣HTTP編碼。

## 範例 {#section-d800cfc31abe46d2a964f8e7929231f1}

**分層模板（帶快取）:**

使用嵌套將快取添加到分層模板。 有限數量的背景影像被高度可變的文本覆蓋。 初始模板字串可能如下所示：

`layer=0&src=$img$&size=300,300&layer=1&text=$txt$`

只需稍作修改，我們就可以預縮放第0層映像並永久快取它，從而減少伺服器負載：

`layer=0&src=is(?src=$img$&size=300,300&cache=on)&layer=1&text=$txt$`

**嵌入Dynamic Media影像渲染請求**

使用儲存在 [!DNL myCatalog/myTemplate];使用Dynamic Media影像渲染為模板第2層生成影像：

`http://server/is/image/myCatalog/myTemplate?layer=2&src=ir(myRenderCatalog/myRenderObject?id=myIdValue&sel=group&src=is(myCatalog/myTexture1?res=30)&res=30)&wid=300`

注意嵌套的大括弧。 影像呈現請求嵌入對影像服務的回叫以檢索可重複紋理。

## 另請參閱 {#section-109a0a9a3b144158958351139c8b8e69}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) 。 [掩碼=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)。 [請求預處理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-preprocessing.md#reference-c27976436bf04194bfbe9adf40ea98e3)，影像渲染引用， [模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)。 [映像服務實用程式](../../../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)
