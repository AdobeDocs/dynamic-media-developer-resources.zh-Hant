---
description: RTF規範允許使用\colortbl指定的RGB顏色值。 每個元件都分別提供\red 、 \green和\blue命令。
seo-description: RTF規範允許使用\colortbl指定的RGB顏色值。 每個元件都分別提供\red 、 \green和\blue命令。
seo-title: 色彩處理
solution: Experience Manager
title: 色彩處理
topic: Scene7 Image Serving - Image Rendering API
uuid: 6c51d204-27ca-4fbd-a297-bf1d04b63a3f
translation-type: tm+mt
source-git-commit: 341693d69fc414dacf984d66e2eaeba2418e663b

---


# 色彩處理{#color-handling}

RTF規範允許使用指定的RGB顏色值 `\colortbl`。 每個元件都分別提供 `\red`、 `\green`和命 `\blue` 令。

專有的RTF擴展命 `\cmykcolortbl` 令允許指定CMYK顏色，每個顏色元件都 `\cyan`提供 `\magenta`、 `\yellow`和 `\black` 命令。

顏色元件 `\colortbl` 值的範圍是0到255。 的組 `\cmykcolortbl` 件值在0到100之間。

RTF擴展命令 `\*\iscolortbl`受支援， `textPs=`它提供了一種方法，可以指定具有標準「影像服務」顏色值的顏色表，並支援全RGB、灰色、CMYK和alpha。 其語法如下：

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* 一或多個IS顏色值，以&#39;;&#39;分隔

可以在同一或RTF字串中指定多種 `text=` 顏色 `textPs=` 表類型。 每個顏色表可以有不同的條目數。 影像伺服會嘗試依此順序尋找顏色：在 `\iscolortbl` 之 `\cmykcolortbl` 前（僅當文字圖層的像素類型為CMYK時） `\colortbl`。 只 `textPs=` 有在需要時，才能在CMYK和RGB之間精確轉換顏色（例如，指定RGB顏色但需要CMYK輸出時）。 如果找不到特定索引值的顏色，則使用預設顏色（黑色）。

有關IS [顏色值](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) 語法的說明，請參閱color。

## Restrictions {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` 不支援 `\*\iscolortbl`。 `textPs=` 不支援 `\cmykcolortbl`。

在轉換Photofonts時，會忽略顏色選取。

## 範例 {#section-0f166bb72bd44479be01131077851142}

允許使用變數控制三種文本顏色，同時在標準RTF文本編輯器中開啟RTF字串時仍顯示顏色預設值。

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
