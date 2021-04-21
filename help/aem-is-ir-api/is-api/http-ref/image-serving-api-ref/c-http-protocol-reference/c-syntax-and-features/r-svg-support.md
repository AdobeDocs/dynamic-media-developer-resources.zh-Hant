---
description: 影像伺服支援可縮放向量圖形(SVG)檔案做為來源資料。 必須符合SVG 1.1。
solution: Experience Manager
title: SVG支援
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---


# SVG支援{#svg-support}

影像伺服支援可縮放向量圖形(SVG)檔案做為來源資料。 必須符合SVG 1.1。

影像服務僅識別靜態SVG內容；動畫、指令碼和其他互動式內容不受支援。

SVG可以指定在允許影像檔案的位置（URL路徑、`src=`和`mask=`）。 點陣化SVG檔案的內容後，就像影像一樣處理。

與影像類似，SVG檔案可以指定為影像目錄條目或相對檔案路徑。

## 替代變數{#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` 替代變數可以包含在SVG檔案中的值字串元素 `<text>` 和任何元素屬性中。

內嵌影像伺服請求查詢部分的重要變數不會直接取代。 請求會附加所有可用的變數定義，這可讓影像伺服在剖析請求時取代變數。

如需詳細資訊，請參閱[替代變數](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)。

## 影像參考{#section-a7680f9e6aca4b1a83560637cc9fac66}

影像可以使用`<image>`元素插入到SVG中。 `<image>`元素的`xlink::href`屬性所參照的影像必須是有效的影像伺服請求。 不允許使用外國URL。

指定完整的影像伺服請求（從`http://`開始）或相對URL（從`/is/image`開始）。 如果指定完整的HTTP路徑，則會從路徑中移除網域名稱，以轉換為相對格式。 使用完整的HTTP路徑可能有其優點，因為它可讓使用協力廠商SVG轉譯器預覽檔案。

>[!NOTE]
>
>本版「影像伺服」中對轉譯影像的支援有限。 只有在傳統「影像伺服」分層和範本化機制不足以達到所需結果的情況下，才應使用SVG中的參照影像。 在任何情況下，都不應使用SVG來產生多影像構圖。

>[!NOTE]
>
>目前，內嵌在SVG中的影像不會自動調整大小。 請確定所有影像參照都包含必要的「影像伺服」命令，以設定所要的影像大小(例如`wid=`)。 如果未明確設定影像大小，則會套用`attribute::DefaultPix`。

## 色彩管理{#section-ea76e2bc4e1842638aa97a2d470c8a68}

所有嵌入在SVG檔案中並通過替代變數傳遞到SVG模板的顏色值都假定存在於`sRgb`顏色空間中。

當影像嵌入到SVG中時，不執行顏色轉換。 為確保色彩的完整性，請務必為所有內嵌的影像要求指定`icc=sRgb`。

點陣化後，SVG影像會像其他影像一樣參與色彩管理。

## 範例 {#section-036cdd45abd449849ee00a8f21788c28}

以下SVG範本說明影像參考和變數的使用。

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

此SVG範本的使用方式如下：

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## 限制{#section-daa5eccd07204aaf993be41e87822d54}

SVG檔案必須獨立，且不得參考任何次要檔案或資源，但「影像伺服」或「影像演算」請求所參照的外部影像除外（請參閱上文）。

僅呈現靜態內容。 動畫、互動功能，例如按鈕等。 可能存在，但可能無法如預期呈現。

目前不支援ICC描述檔色彩規格。

`<script>` 元素可能存在，但一律忽略。

## 另請參閱 {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [SVG 1.1規格](http://www.w3.org/TR/SVG11/)
