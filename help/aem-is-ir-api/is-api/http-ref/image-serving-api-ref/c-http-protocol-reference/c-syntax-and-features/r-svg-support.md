---
description: 影像伺服支援可縮放向量圖形(SVG)檔案作為源資料。 需要符合SVG 1.1。
solution: Experience Manager
title: SVG支援
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 60e40195-710f-4f03-b152-52eaa10c5b21
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# SVG支援{#svg-support}

影像伺服支援可縮放向量圖形(SVG)檔案作為源資料。 需要符合SVG 1.1。

「影像伺服」僅識別靜態SVG內容；不支援動畫、指令碼和其他互動式內容。

可以在允許影像檔案的位置指定SVG（URL路徑、`src=`和`mask=`）。 柵格化SVG檔案的內容後，其處理方式就像影像一樣。

與影像類似，SVG檔案可以指定為影像目錄條目或相對檔案路徑。

## 替代變數 {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` 替代變數可以包含在SVG檔案中的值字串元素 `<text>` 和任何元素屬性中。

內嵌影像伺服請求的查詢部分中的重要變數不會直接取代。 反之，所有可用的變數定義都會附加至請求，讓影像伺服在剖析請求時能取代變數。

如需詳細資訊，請參閱[替代變數](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)。

## 影像參考 {#section-a7680f9e6aca4b1a83560637cc9fac66}

可使用`<image>`元素將影像插入SVG中。 `<image>`元素的`xlink::href`屬性所參考的影像必須是有效的影像服務請求。 不允許使用外國URL。

指定完整的「影像伺服」請求（以`http://`開頭），或以`/is/image`開頭的相對URL。 如果指定了完整的HTTP路徑，則將從路徑中刪除域名，以轉換為相對格式。 使用完整HTTP路徑可能有其優點，因為它可讓檔案以協力廠商SVG轉譯器預覽。

>[!NOTE]
>
>此版本的「影像伺服」僅支援轉譯影像。 只有在傳統影像服務分層和模板機制不足以達到期望結果的情況下，才應使用從SVG內引用影像。 在任何情況下，都不應使用SVG來產生多影像複合。

>[!NOTE]
>
>目前不會自動調整SVG中嵌入的影像大小。 請確定所有影像參數都包含必要的「影像伺服」命令，以設定所需的影像大小(例如`wid=`)。 如果未明確設定影像大小，則將應用`attribute::DefaultPix`。

## 色彩管理 {#section-ea76e2bc4e1842638aa97a2d470c8a68}

所有嵌入在SVG檔案中並通過替代變數傳遞到SVG模板的顏色值都假定存在於`sRgb`顏色空間中。

將影像嵌入到SVG中時，不執行顏色轉換。 為確保色彩保真度，請務必為所有內嵌的影像要求指定`icc=sRgb`。

光柵化後，SVG影像與任何其他影像一樣參與色彩管理。

## 範例 {#section-036cdd45abd449849ee00a8f21788c28}

以下SVG範本說明影像參考和變數的使用。

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

此SVG模板的使用方式如下：

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## 限制 {#section-daa5eccd07204aaf993be41e87822d54}

SVG檔案必須是獨立的，且不得參考任何次要檔案或資源，但與影像伺服或影像呈現請求參照的外部影像除外（請參閱上文）。

只會轉譯靜態內容。 動畫、互動式功能，如按鈕等。 可能存在，但可能無法如預期呈現。

目前不支援ICC設定檔色彩規格。

`<script>` 元素可能存在，但一律會忽略。

## 另請參閱 {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [SVG 1.1規範](http://www.w3.org/TR/SVG11/)
