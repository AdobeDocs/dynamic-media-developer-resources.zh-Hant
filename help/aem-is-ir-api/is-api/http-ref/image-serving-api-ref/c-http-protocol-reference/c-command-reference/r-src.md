---
description: 圖層影像。
solution: Experience Manager
title: src
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 3%

---


# src{#src}

圖層影像。

` src= *`objectentedRequest`*|{[is|ir|fxg]'{' *``*'}'}`

<table id="simpletable_59104309B8284B21ABCE7DC95BF5A273"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> object </span> </p> </td> 
  <td class="stentry"> <p>影像物件。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> nestedRequest  </span> </p> </td> 
  <td class="stentry"> <p>巢狀影像伺服、影像演算或外部請求。 </p> </td> 
 </tr> 
</table>

## 說明 {#section-59ec6dc2afcb43efb34dbb0f7733543f}

指定影像圖層的來源影像。

*`object`* 可以是目錄條目或影像/SVG檔案。

請參閱[object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)。

巢狀或內嵌的請求會以大括弧括住。 將內嵌影像伺服請求前置詞為`is`、內嵌影像演算請求前置詞為`ir`，以及FXG圖形演算請求前置詞為`fxg`。 如果未指定前置詞，則假定對外部伺服器的請求。

請參閱[請求巢狀內嵌](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)。

## 屬性 {#section-2c22bb89a35d470f833df8ba898efd93}

層屬性。 如果`layer=comp`，則套用至`layer=0`。 與`text=`和`textPs=`在同一層中互斥；上次出現`text=`、`textPs=`或`src=`的情況會優先，並判斷這是影像還是文字圖層。 被效果圖層忽略。

*`object`*可能無法解析到其`catalog::Modifier`中包含`src=`或`mask=`命令的其他目錄記錄。 （使用請求巢狀以產生類似的效果）。

`is`、`ir`和`fxg`字首區分大小寫。

## 預設 {#section-a92f3882041b4d43ae2caf014647165f}

對於第0層，如果未指定`src=`，則使用URL路徑元件中的物件。 沒有其他圖層的預設值。

## 另請參閱 {#section-e467e03330564796932ac081f1c9c1d0}

[目錄：:Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ，屬 [性：RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),RootPath [, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f)Ps=Text，遮色片= [Ps](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) [ ObjectMask, ObjectMeding, Templates Embedding, Request Nesting and Request Nesting and Request](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
