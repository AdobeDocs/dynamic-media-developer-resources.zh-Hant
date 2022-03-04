---
description: 影像服務支援可縮放向量圖形(SVG)檔案作為源資料。 必須符合SVG1.1。
solution: Experience Manager
title: SVG支援
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 60e40195-710f-4f03-b152-52eaa10c5b21
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 0%

---

# SVG支援{#svg-support}

影像服務支援可縮放向量圖形(SVG)檔案作為源資料。 必須符合SVG1.1。

影像服務僅識別靜態SVG內容；不支援動畫、指令碼和其他交互內容。

SVG可以指定任何允許的影像檔案(URL路徑、 `src=`, `mask=`)。 在柵格化SVG檔案的內容後，它就像影像一樣處理。

與影像類似，SVG檔案可以指定為影像目錄條目或相對檔案路徑。

## 替代變數 {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` 替換變數可以包含在值字串中的SVG檔案中 `<text>` 元素和任何元素屬性。

嵌入式影像服務請求的查詢部分中的重要變數不會直接替換。 相反，所有可用的變數定義都附加到請求中，這允許影像服務在分析請求時替換變數。

請參閱 [替代變數](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a) 的雙曲餘切值。

## 影像引用 {#section-a7680f9e6aca4b1a83560637cc9fac66}

影像可以使用 `<image>` 的子菜單。 由 `xlink::href` 屬性 `<image>` 元素必須是有效的影像服務請求。 不允許使用外來URL。

指定完整的映像服務請求，從 `http://`，或相對url，以 `/is/image`。 如果指定了完整的HTTP路徑，則從路徑中刪除域名以轉換為相對格式。 使用完整HTTP路徑可能是有優勢的，因為它允許使用第三方SVG呈現器預覽檔案。

>[!NOTE]
>
>在此版本的影像服務中對渲染影像的支援有限。 僅在傳統影像服務分層和模板機制不足以達到預期結果的情況下，才應使用SVG內的引用影像。 在任何情況下都不應使用SVG來生成多影像複合材料。

>[!NOTE]
>
>此時，嵌入在SVG中的影像不會自動調整大小。 確保所有影像參照都包括設定所需影像大小所需的「影像服務」命令(例如， `wid=`)。 如果未顯式設定影像大小， `attribute::DefaultPix` 的子菜單。

## 色彩管理 {#section-ea76e2bc4e1842638aa97a2d470c8a68}

所有嵌入在SVG檔案中並通過替換變數傳遞給SVG模板的顏色值都假定存在於 `sRgb` 顏色空間。

當影像嵌入到SVG中時不執行顏色轉換。 要確保顏色保真度，請確保指定 `icc=sRgb` 所有嵌入式映像請求。

光柵化後，SVG影像像其他影像一樣參與色彩管理。

## 範例 {#section-036cdd45abd449849ee00a8f21788c28}

以下SVG模板說明了影像引用和變數的使用。

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

此SVG模板可能使用如下：

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## 限制 {#section-daa5eccd07204aaf993be41e87822d54}

SVG檔案必須是獨立檔案，並且不得引用任何次檔案或資源，但與「影像服務」或「影像呈現」請求一起引用的外部影像除外（請參閱上文）。

只呈現靜態內容。 動畫、互動式功能，如按鈕等。 可能存在，但可能未按預期呈現。

目前不支援基於ICC配置檔案的顏色規範。

`<script>` 元素可能存在，但始終被忽略。

## 另請參閱 {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) 。 [掩碼=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)。 [SVG1.1規範](https://www.w3.org/TR/SVG11/)
