---
description: RTF規範允許使用&bsol;colortbl指定的RGB顏色值。 每個元件都分別提供&bsol;red、&bsol;green和&bsol;blue命令。
solution: Experience Manager
title: 顏色處理
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# 顏色處理{#color-handling}

RTF規範允許使用指定的RGB顏色值 `\colortbl`。 每個元件分別與 `\red`。 `\green`, `\blue` 的雙曲餘切值。

專有的RTF擴展命令 `\cmykcolortbl` 允許指定CMYK顏色，每個顏色元件都 `\cyan`。 `\magenta`。 `\yellow`, `\black` 的雙曲餘切值。

顏色元件值 `\colortbl` 在0到255之間。 元件值 `\cmykcolortbl` 在0到100之間。

RTF擴展命令 `\*\iscolortbl`，支援 `textPs=`，提供了一種指定帶有標準「影像服務」顏色值的顏色表的方法，該顏色表支援全RGB、灰度、CMYK和Alpha。 它具有以下語法：

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* 一個或多個IS顏色值，用「；」分隔

可以在同一個中指定多種顏色表類型 `text=` 或 `textPs=` RTF字串。 每個顏色表可以有不同數量的條目。 影像服務將嘗試按以下順序查找顏色： `\iscolortbl` 先 `\cmykcolortbl` （僅當文本圖層的像素類型為CMYK時） `\colortbl`。 對於 `textPs=` 只是，如果需要，顏色會在CMYK和RGB之間精確轉換(例如，指定RGB顏色但需要CMYK輸出)。 如果找不到特定索引值的顏色，則使用預設顏色（黑色）。

請參閱 [顏色](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) 的子菜單。

## 限制 {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` 不支援 `\*\iscolortbl`。 `textPs=` 不支援 `\cmykcolortbl`。

呈現「照片字型」時，將忽略顏色選擇。

## 範例 {#section-0f166bb72bd44479be01131077851142}

允許使用變數控制三種文本顏色，同時在標準RTF文本編輯器中開啟RTF字串時仍顯示顏色預設值。

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
