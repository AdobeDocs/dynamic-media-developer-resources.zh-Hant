---
description: 圖層影像。
seo-description: 圖層影像。
seo-title: src
solution: Experience Manager
title: src
topic: Scene7 Image Serving - Image Rendering API
uuid: b4396848-b992-4371-a8ae-4ff1781ae1be
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

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
  <td class="stentry"> <p> <span class="varname"> nestedRequest </span> </p> </td> 
  <td class="stentry"> <p>巢狀影像伺服、影像演算或外部請求。 </p> </td> 
 </tr> 
</table>

## 說明 {#section-59ec6dc2afcb43efb34dbb0f7733543f}

指定影像圖層的來源影像。

*`object`* 可以是目錄條目或影像/SVG檔案。

請參 [閱對象](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)。

巢狀或內嵌的請求會以大括弧括住。 將內嵌的影像伺服要求前置 `is`詞為內嵌的影像呈現要求、內嵌的影像 `ir`呈現要求以及FXG圖形呈現要求 `fxg`。 如果未指定前置詞，則假定對外部伺服器的請求。

請參 [閱請求巢狀和內嵌](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)。

>[!NOTE]
>
>FXG圖形演算僅適用於Scene7代管環境，可能需要額外授權。 如需詳細資訊，請連絡Scene7支援。

## 屬性 {#section-2c22bb89a35d470f833df8ba898efd93}

層屬性。 套用至 `layer=0` 如果 `layer=comp`。 在同一層 `text=` 中 `textPs=` 互斥，最後一次出現 `text=`、 `textPs=`或 `src=` 優先，並判斷這是影像還是文字圖層。 被效果圖層忽略。

*`object`*可能無法解析至其他目錄記錄，其中包含 `src=` 或 `mask=` 命令 `catalog::Modifier`。 （使用請求巢狀以產生類似的效果）。

字 `is`首、 `ir`和 `fxg` 前置詞區分大小寫。

## 預設 {#section-a92f3882041b4d43ae2caf014647165f}

對於第0層，如果未指定，則會使用URL路徑元件 `src=` 中的物件。 沒有其他圖層的預設值。

## 另請參閱 {#section-e467e03330564796932ac081f1c9c1d0}

[目錄：:Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [屬性：RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),RootPath [,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f)Ps=Text，遮色片= [Ps](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)[ObjectMask, ObjectMedting, Templates Embedding and Request Nesting and Request Resenting and Request](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
