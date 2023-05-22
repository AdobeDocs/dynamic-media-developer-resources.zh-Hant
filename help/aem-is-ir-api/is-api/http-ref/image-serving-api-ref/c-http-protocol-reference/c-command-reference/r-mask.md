---
description: 影像蒙版。 指定要用作未關聯蒙版的單獨蒙版影像。
solution: Experience Manager
title: 掩模
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5785844b-945b-4dd0-ac59-efbf1360b7cd
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 1%

---

# 掩模{#mask}

影像蒙版。 指定要用作未關聯蒙版的單獨蒙版影像。

`mask= *`對象`*|{[is|ir]'{' *`嵌套請求`*'}'}`

<table id="simpletable_F5A8CD8D7E9B48DAB3C8184E8FE60D9B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> object</span> </p></td> 
  <td class="stentry"> <p>要用作影像或圖層蒙版的影像對象。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 嵌套請求</span> </p></td> 
  <td class="stentry"> <p>嵌套影像服務、影像呈現或外部請求。 </p></td> 
 </tr> 
</table>

*`object`* 可以是目錄條目或影像/SVG檔案。 可以為影像層和實色層指定。

如果 *`object`* 解析為影像目錄條目， `catalog::MaskPath` 或 `catalog::MaskPath` 未定義 `catalog::Path` 的子菜單。 如果 *`object`* 不解析為目錄條目，則會將其解釋為檔案路徑。

在所有情況下，如果源影像具有Alpha通道，則使用它。 否則，在將影像用作圖層蒙版之前，如有必要，將影像轉換為灰度。

如果蒙版連接到實色層，則可以使用與影像層中影像使用的相同規則對其進行裁剪和縮放。 `size=`。 `scale=`或 `res=` 可以用來縮放蒙版。

也可以以 *`nestedRequest`*。 嵌套或嵌入的請求由大括弧括起來。 為嵌入式影像服務請求添加前置詞 `is` 和嵌入式影像呈現請求 `ir`。 如果未指定前置詞，則假定對外部伺服器的請求。 請參閱 [請求嵌套和嵌入](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b) 的雙曲餘切值。

## 屬性 {#section-a093043dc249423b8ae322cefb0d545d}

影像或圖層屬性。 如果為 `layer=comp`。 被效果層忽略。

*`object`* 不能解析為包含 `src=` 或 `mask=` 命令 `catalog::Modifier`。

的 `is` 和 `ir` 前置詞不區分大小寫。

## 預設 {#section-10cf793c665f49deb1b248faa3b618a9}

如果 `mask=` 未顯式指定，如果圖層影像與目錄條目關聯，則 `catalog::MaskPath` 的子菜單。 否則，如果存在，則使用層影像的α通道。 如果沒有Alpha通道，則圖層沒有蒙版，並且圖層矩形被渲染為完全不透明。

## 範例 {#section-1bbe623f7c744bdf97b596458d8e7ea3}

使用多個單獨的蒙版來著色影像的不同區域。 已著色的被遮罩區域被層疊在原始未修改影像上：

`http://server/myRootId/myImageId?wid=500& layer=1&src=myImageId&mask=myMask1&op_colorize=200,0,0& layer=2&src=myImageId&mask=myMask2&op_colorize=0,200,0& layer=3&src=myImageId&mask=myMask3&op_colorize=0,0,200`

## 另請參閱 {#section-7ed5201d91594e5f872438a92eaf1c89}

[掩碼使用=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464) 。 [目錄：:MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)。 [對象](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) 。 [請求嵌套和嵌入](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
