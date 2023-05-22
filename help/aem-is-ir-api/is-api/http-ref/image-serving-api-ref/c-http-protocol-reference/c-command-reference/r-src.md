---
description: 圖層影像。
solution: Experience Manager
title: 高
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 88b89e70-59cf-4fb9-bbe7-0ac5eff792f1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 2%

---

# 高{#src}

圖層影像。

` src= *`對象`*|{[is|ir|fxg]'{' *`嵌套請求`*'}'}`

<table id="simpletable_59104309B8284B21ABCE7DC95BF5A273"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> object </span> </p> </td> 
  <td class="stentry"> <p>影像對象。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 嵌套請求 </span> </p> </td> 
  <td class="stentry"> <p>嵌套影像服務、影像呈現或外部請求。 </p> </td> 
 </tr> 
</table>

## 說明 {#section-59ec6dc2afcb43efb34dbb0f7733543f}

指定影像圖層的源影像。

*`object`* 可以是目錄條目或影像/SVG檔案。

請參閱 [對象](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)。

嵌套或嵌入的請求由大括弧括起來。 為嵌入式影像服務請求添加前置詞 `is`，嵌入的影像呈現請求 `ir`，以及FXG圖形渲染請求 `fxg`。 如果未指定前置詞，則假定對外部伺服器的請求。

請參閱 [請求嵌套和嵌入](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)。

## 屬性 {#section-2c22bb89a35d470f833df8ba898efd93}

層屬性。 應用於 `layer=0` 如果 `layer=comp`。 與 `text=` 和 `textPs=` 同一層；最後一次 `text=`。 `textPs=`或 `src=` 並確定這是影像還是文本圖層。 被效果層忽略。

*`object`*可能無法解析到包含 `src=` 或 `mask=` 命令 `catalog::Modifier`。 （使用請求嵌套來達到類似效果。）

的 `is`。 `ir`, `fxg` 前置詞區分大小寫。

## 預設 {#section-a92f3882041b4d43ae2caf014647165f}

對於第0層，使用URL路徑元件中的對象 `src=` 未指定。 其它層沒有預設值。

## 另請參閱 {#section-e467e03330564796932ac081f1c9c1d0}

[目錄：：路徑](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) 。 [屬性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)。 [文本=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f)。 [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)。 [掩碼=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)。 [對象](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)。 [模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)。 [請求嵌套和嵌入](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
