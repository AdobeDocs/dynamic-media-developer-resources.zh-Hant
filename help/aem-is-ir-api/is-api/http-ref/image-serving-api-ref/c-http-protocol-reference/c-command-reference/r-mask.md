---
description: 影像遮色片。 指定單獨的遮色片影像，用作未關聯的遮色片。
seo-description: 影像遮色片。 指定單獨的遮色片影像，用作未關聯的遮色片。
seo-title: 遮罩
solution: Experience Manager
title: 遮罩
topic: Scene7 Image Serving - Image Rendering API
uuid: 2dc14d20-f02a-4a77-9b73-0c01e10d448d
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# mask{#mask}

影像遮色片。 指定單獨的遮色片影像，用作未關聯的遮色片。

`mask= *`objectentedRequest`*|{[is|ir]'{' *``*'}'}`

<table id="simpletable_F5A8CD8D7E9B48DAB3C8184E8FE60D9B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> object</span> </p></td> 
  <td class="stentry"> <p>要用作影像或圖層蒙版的影像對象。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> nestedRequest</span> </p></td> 
  <td class="stentry"> <p>巢狀影像伺服、影像演算或外部請求。 </p></td> 
 </tr> 
</table>

*`object`* 可以是目錄條目或影像/SVG檔案。 可以為影像圖層和純色圖層指定。

如果 *`object`* 解析為影像目錄項目， `catalog::MaskPath` 則會使用，或 `catalog::MaskPath` 者，如果未定義，則會使 `catalog::Path` 用。 如果 *`object`* 未解析為目錄條目，則會將其解釋為檔案路徑。

在所有情況下，如果來源影像具有Alpha色版，則會使用它。 否則，在將影像用作圖層蒙版之前（如果需要），將影像轉換為灰度。

如果遮色片附著在純色圖層上，則可使用影像圖層中影像所用的相同規則來裁切和縮放遮色片。 `size=`、 `scale=`或 `res=` 可用於縮放遮色片。

圖層遮色片也可以指定為 *`nestedRequest`*。 巢狀或內嵌的請求會以大括弧括住。 將內嵌的影像伺服請求前置為首 `is` 碼，並將內嵌的影像演算請求前置為首 `ir`碼。 如果未指定前置詞，則假定對外部伺服器的請求。 如需詳細 [資訊，請參閱「請求巢狀和內嵌](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b) 」。

## 屬性 {#section-a093043dc249423b8ae322cefb0d545d}

影像或圖層屬性。 如果適用，則套用至圖層0 `layer=comp`。 被效果圖層忽略。

*`object`* 不能解析為目錄記錄，該目錄記錄包含 `src=` 或 `mask=` 命令 `catalog::Modifier`。

前置詞 `is` 和 `ir` 前置詞不區分大小寫。

## 預設 {#section-10cf793c665f49deb1b248faa3b618a9}

如果 `mask=` 未明確指定，並且圖層影像與目錄條目相關聯，則使用 `catalog::MaskPath` 該圖層。 否則，如果存在，則使用圖層影像的Alpha通道。 如果沒有Alpha通道，則圖層沒有遮色片，並且圖層矩形會呈現為完全不透明。

## 範例 {#section-1bbe623f7c744bdf97b596458d8e7ea3}

使用數個不同的遮色片，為影像的不同區域上色。 已上色的遮色片區域會在原始未修改影像上分層：

`http://server/myRootId/myImageId?wid=500& layer=1&src=myImageId&mask=myMask1&op_colorize=200,0,0& layer=2&src=myImageId&mask=myMask2&op_colorize=0,200,0& layer=3&src=myImageId&mask=myMask3&op_colorize=0,0,200`

## 另請參閱 {#section-7ed5201d91594e5f872438a92eaf1c89}

[maskUse=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464) , [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md), [object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) , [Request Nesting and Embedding](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
