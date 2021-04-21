---
description: RTF規範允許使用&bsol;colortbl指定的RGB顏色值。 每個元件分別提供&bsol;red、&bsol;green和&bsol;blue命令。
solution: Experience Manager
title: 色彩處理
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---


# 色彩處理{#color-handling}

RTF規範允許使用`\colortbl`指定的RGB顏色值。 每個元件分別提供`\red`、`\green`和`\blue`命令。

專有的RTF擴展命令`\cmykcolortbl`允許指定CMYK顏色，每個顏色元件都提供`\cyan`、`\magenta`、`\yellow`和`\black`命令。

`\colortbl`的顏色元件值在0到255之間。 `\cmykcolortbl`的元件值在0到100之間。

RTF擴展命令`\*\iscolortbl`受`textPs=`支援，它提供了一種指定帶有標準「影像服務」顏色值的顏色表的方法，該顏色表支援全RGB、灰色、CMYK和alpha。 其語法如下：

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* 一或多個IS顏色值，以&#39;;&#39;分隔

可以在相同的`text=`或`textPs=` RTF字串中指定多種顏色表類型。 每個顏色表可以有不同的條目數。 影像伺服會嘗試依此順序尋找顏色：`\cmykcolortbl`之前的`\iscolortbl`（僅當文字圖層的像素類型為CMYK時）在`\colortbl`之前。 僅適用於`textPs=`，如果需要，顏色會在CMYK和RGB之間精確轉換（例如，指定RGB顏色但需要CMYK輸出時）。 如果找不到特定索引值的顏色，則使用預設顏色（黑色）。

有關IS顏色值語法的說明，請參閱[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)。

## 限制{#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` 不支援 `\*\iscolortbl`。`textPs=` 不支援 `\cmykcolortbl`。

在轉換Photofonts時，會忽略顏色選取。

## 範例 {#section-0f166bb72bd44479be01131077851142}

允許使用變數控制三種文本顏色，同時在標準RTF文本編輯器中開啟RTF字串時仍顯示顏色預設值。

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
