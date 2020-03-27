---
description: 將影像與檢視對齊。 在wid=和hei=定義的視圖矩形內對齊合成影像（如果也指定了scl=，則可能在縮放後）。
seo-description: 將影像與檢視對齊。 在wid=和hei=定義的視圖矩形內對齊合成影像（如果也指定了scl=，則可能在縮放後）。
seo-title: 對齊
solution: Experience Manager
title: 對齊
topic: Scene7 Image Serving - Image Rendering API
uuid: 91940bd4-8e2b-4949-a76d-31cd238783bc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# align{#align}

將影像與檢視對齊。 在wid=和hei=定義的視圖矩形內對齊合成影像（如果也指定了scl=，則可能在縮放後）。

` align= *`水`*, *`平`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 霍里 </span> 茲 </span> </p> </td> 
  <td class="stentry"> <p>水準對齊（實數、-1.0...1.0） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> vert </span></span> </p> </td> 
  <td class="stentry"> <p>垂直對齊（實數、-1.0...1.0） </p> </td> 
 </tr> 
</table>

指 `align=-1,-1` 定將合成影像的左上角與檢視的左上角對齊，指定 `align=1,1` 將影像的右下角與檢視的右下角對齊。 對於標準影像和縮圖要求，複合影像資料未涵蓋的檢視任何區域都會填入 `bgc=`。

## 屬性 {#section-3fbec8206fc944eda4746d8be84f3b41}

檢視屬性。 ( `align=` 也用來定義水印影像與套用水印的複合影像之間的對齊方式)。不論目前的圖層設定如何，都適用。 如果僅指定其中一 `wid=` 個和 `hei=` ，以及指定或時，則 `fit=constrain` 忽略 `fit=stretch`。

## 預設 {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`，這會將影像置於檢視矩形中。

## 範例 {#section-2c9447aa2e184fb8ab1a4370dc61d554}

下列要求適 `myImage` 合200x200像素的檢視矩形。

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

如果 `myImage` 正方形，則填充整個視圖矩形。 如果 `myImage` 有縱向長寬比，則會縮放為200像素高，並在檢視中水準置中。 如 `myImage` 果有橫向長寬比，則會縮放為200像素寬，並與檢視的上邊緣對齊。 在所有情況下，傳回的影像大小都是200x200像素；縮放後未覆蓋的任何空 `myImage` 間都會填 `attribute::BkgColor` 入（指定bgc=以動態控制背景顏色）。

## 另請參閱 {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , hei= [, fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), bgc= [,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)[水印](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
