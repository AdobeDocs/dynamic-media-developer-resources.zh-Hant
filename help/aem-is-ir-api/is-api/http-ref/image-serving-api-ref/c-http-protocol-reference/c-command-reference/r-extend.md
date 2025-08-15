---
title: 延伸
description: 延伸圖層。 增加圖層邊界或裁切圖層矩形。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03db6555-6851-49d4-b0de-5570bf56ad76
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 1%

---

# 延伸{#extend}

延伸圖層。 增加圖層邊界或裁切圖層矩形。

`extend= *`左`*, *`上`*, *`右`*, *`下`*`

`extendN= *`leftN`*, *`topN`*, *`rightN`*, *`bottomN`*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">靠左、靠上、靠下、靠右</span></span> </p></td> 
  <td class="stentry"> <p>要增加至（或從中移除，如果值為負值）圖層矩形(int、int、int、int、int)的左邊緣、上邊緣、右邊緣與下邊緣的畫素數。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> leftN，topN，bottomN，rightN</span></span> </p></td> 
  <td class="stentry"> <p>在圖層矩形的左邊、上邊、右邊和底邊增加（或移除，如果值為負值）的空間量，以相對於原始圖層矩的大小（實數、實數、實數、實數）的標準化數量表示。 </p></td> 
 </tr> 
</table>

`extend=`套用至&#x200B;*之後的圖層*&#x200B;影像( `crop=`)並已套用所有圖層轉換，包括`rotate=`。

延伸區域已填滿`bgColor=`，如果未指定，則保持透明。

在套用圖層轉換（包括`extendN=`）之後，`rotate=`的引數值會相對於圖層矩形的大小正規化。

## 屬性 {#section-8fc94de871f841f3bf5e1df135972ca9}

圖層屬性。 套用至圖層0 （若`layer=comp`）。 被效果圖層忽略。

## 預設 {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`，因為圖層矩形沒有變更。

## 範例 {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**裁切影像，然後新增5畫素寬的紅色邊框：**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**將影像縮放至200畫素寬度，並將標題文字新增至影像上方的30畫素邊界。**

請注意，複合影像的高度會依影像的外觀比例而有所不同。

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## 另請參閱 {#section-2d9572be32ca4602b60920b3810f3638}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ， [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)， [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)， [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)， [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
