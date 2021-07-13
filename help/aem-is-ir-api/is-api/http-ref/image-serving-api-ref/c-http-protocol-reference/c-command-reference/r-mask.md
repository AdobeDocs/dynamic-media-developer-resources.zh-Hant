---
description: 影像遮色片。 指定要用作未關聯掩碼的單獨掩碼影像。
solution: Experience Manager
title: 遮罩
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5785844b-945b-4dd0-ac59-efbf1360b7cd
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 1%

---

# 遮罩{#mask}

影像遮色片。 指定要用作未關聯掩碼的單獨掩碼影像。

`mask= *``*|{[is|ir]'{' *`objectnestedRequest`*'}'}`

<table id="simpletable_F5A8CD8D7E9B48DAB3C8184E8FE60D9B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> object</span> </p></td> 
  <td class="stentry"> <p>要用作影像或圖層遮色片的影像對象。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> nestedRequest</span> </p></td> 
  <td class="stentry"> <p>巢狀影像提供、影像轉譯或外部要求。 </p></td> 
 </tr> 
</table>

*`object`* 可以是目錄項目或影像/SVG檔案。可為影像層和實色層指定。

如果&#x200B;*`object`*&#x200B;解析為影像目錄條目，則使用`catalog::MaskPath`，或者，如果未定義`catalog::MaskPath`，則使用`catalog::Path`。 如果&#x200B;*`object`*&#x200B;未解析為目錄項，則會將其解釋為檔案路徑。

在所有情況下，如果源影像具有Alpha通道，則會使用它。 否則，在將影像用作圖層蒙版之前，如果需要，該影像將轉換為灰度。

如果蒙版附加到實色層，則可以使用用於影像層中影像的相同規則來裁剪和縮放蒙版。 `size=`、  `scale=`或 `res=` 可用來縮放遮色片。

也可以以&#x200B;*`nestedRequest`*&#x200B;的形式指定圖層蒙版。 巢狀或內嵌的要求會以大括弧括住。 為內嵌影像伺服請求加上`is`前置詞，並為內嵌影像呈現請求加上`ir`前置詞。 如果未指定前置詞，則假定對外部伺服器的請求。 有關詳細資訊，請參閱[請求嵌套和嵌入](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)。

## 屬性 {#section-a093043dc249423b8ae322cefb0d545d}

影像或圖層屬性。 如果`layer=comp`，則應用於層0。 被效果層忽略。

*`object`* 不能解析為目錄記錄，其中包 `src=` 含 `mask=` 或命 `catalog::Modifier`令。

`is`和`ir`前置詞不區分大小寫。

## 預設 {#section-10cf793c665f49deb1b248faa3b618a9}

如果未顯式指定`mask=`，並且如果層影像與目錄項相關聯，則使用`catalog::MaskPath`。 否則，如果存在，則使用層影像的α通道。 如果沒有Alpha通道，則圖層沒有蒙版，並且圖層矩形呈現為完全不透明。

## 範例 {#section-1bbe623f7c744bdf97b596458d8e7ea3}

使用多個單獨的蒙版來著色影像的不同區域。 已著色的被遮罩區域被層疊在原始未修改的影像上：

`http://server/myRootId/myImageId?wid=500& layer=1&src=myImageId&mask=myMask1&op_colorize=200,0,0& layer=2&src=myImageId&mask=myMask2&op_colorize=0,200,0& layer=3&src=myImageId&mask=myMask3&op_colorize=0,0,200`

## 另請參閱 {#section-7ed5201d91594e5f872438a92eaf1c89}

[maskUse=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464) ,  [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md),  [object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) ,  [Request Enseting and Embedding](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
